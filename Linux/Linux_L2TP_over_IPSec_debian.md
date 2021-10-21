# Using L2TP in Debian operates as follows

```The network administrator will provide you with information```

```txt
Type VPN : L2TP over IPSec
Server address : 123.123.123.123 (Replace 123.123.123.123 in the configuration file with your server address)
Account Name :XXX
Password : XXX
Shared Secret: XXXX
```

```Install `IPSec` and `L2TP` related packages```

```bash
sudo apt install strongswan xl2tpd
```

```After this, the following packages should be installed```

```bash
libip4tc0 libip6tc0 libpcap0.8 libprocps6 libstrongswan
libstrongswan-standard-plugins ppp procps strongswan strongswan-charon
strongswan-libcharon strongswan-starter xl2tpd
```

```Setup `IPSec` tunnel using `strongswan` ```


```Setup IPSec VPN tunnel in `/etc/ipsec.conf` ```

```bash
config setup

conn vpninterface0
    keyexchange = ikev2
    authby = secret
    auto = add
    keyingtries = 3
    dpddelay = 30
    dpdtimeout = 120
    dpdaction = clear
    rekey = yes
    ikelifetime = 8h
    keylife = 1h
    type = transport
    left = %defaultroute
    leftprotoport = 17/1701
    right = 123.123.123.123
    rightprotoport = 17/1701
    ike=aes128-sha256-modp2048
    esp=aes128-modp2048
```

```Setup PSK authentication in `/etc/ipsec.secrets`, replace content in quote (exclusive) with PSK above:```

```: PSK "Shared Secret"```

```Setup `L2TP` connection in `IPSec` tunnel```

`/etc/xl2tpd/xl2tpd.conf`

    [global]
    debug state = no
    debug tunnel = no
    debug avp = no
    debug network = no
    debug packet = no
    
    [lac vpninterface0]
    lns = 123.123.123.123
    ppp debug = no
    pppoptfile = /etc/ppp/option.client
    length bit = yes
    require chap = yes
    refuse pap = yes
    require authentication = yes
    name = l2tpd

`/etc/ppp/option.client`, this file should have 600 permission (`sudo chmod 600 /etc/ppp/option.client`)

    ipcp-accept-local
    ipcp-accept-remote
    noccp
    noauth
    mtu 1410
    mru 1410
    nodefaultroute
    usepeerdns
    #lock
    name (your user name)   # replace content in parenthesis (inclusive) with infomation above
    password (your secret password) # dito

```Check that `xl2tpd.service` and `strongswan.service` are running```
```bash
systemctl status strongswan.service xl2tpd.service
```
```Connect to VPN tunnel```
```bash
sudo ipsec up vpninterface0   # start IPSec connection
```
```You should see something like `connection 'vpninterface0' established successfully`. Now you can connect to the L2TP connection:```
```bash
printf 'c vpninterface0\n' | sudo tee /run/xl2tpd/l2tp-control
```
```After the above command, there should be a new interface (usually named) `ppp0` show up when running `ip addr`. Add a static route to your route table:```
```bash
    sudo ip route add 10.0.0.0/24 via 10.111.112.2 dev ppp0   # interface name should be the same as the one you see after the above command
```
```If "pppX" doesn't appear, please restart both `strongswan` and `xl2tpd` services and try again.```
```bash
sudo systemctl restart strongswan.service xl2tpd.service
```
```After this, you should be able to get response when `ping` a host address behind the LAN your VPN connected to.```
```bash
ping yourComputerAddress # Or a hostname on the other end of the tunnel
```
```Disconnect from VPN tunnel```
```bash
printf 'd vpninterface0\n' | sudo tee /run/xl2tpd/l2tp-control   # disconnect L2TP, after this, "ppp0" 
```
```should disappear```

```Script contributed to help you connect and disconnect to VPN```

````You can source the following script and use the function inside to connect and disconnect the VPN tunnel.```
```bash
	dr_vpn_connect() {
	  if pgrep -x "xl2tpd" > /dev/null
	  then
		sudo pkill -9 xl2tpd
	  fi
	  sudo ipsec restart
	  sleep 1
	  sudo xl2tpd
	  sleep 1
	  sudo ipsec up vpninterface0
	  sleep 1
	  printf 'c vpninterface0\n' | sudo tee /run/xl2tpd/l2tp-control
	  sleep 4 # waiting a little bit before setting up routes seem to help avoid 'Cannot find device "ppp0"'
	  dr_vpn_routes
	}

	dr_vpn_routes() {
	  sudo ip route add 10.0.0.0/24 via 10.111.112.2 dev ppp0
	}

	dr_vpn_disconnect() {
	  printf 'd vpninterface0\n' | sudo tee /run/xl2tpd/l2tp-control
	  sudo ipsec down vpninterface0
	  sudo pkill -9 xl2tpd
	}
```