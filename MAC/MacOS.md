# MAC_OS Configuration L2TP over IPSec VPN
[From Apple support](https://support.apple.com/guide/mac-help/change-options-l2tp-ipsec-vpn-connections-mac-mh11941/mac)

```The network administrator will provide you with information```

```txt
Type VPN : L2TP over IPSec
Server address : XXX
Account Name :XXX
Password : XXX
Shared Secret: XXXX
```

```Open network preference```

> Step

```bash

1.  On your Mac, choose Apple menu  > System Preferences, then click Network.
    
2.  Select your VPN service in the list at the left.

    Should choose 'L2tp/IPSec'，Due to the system version, you may need to choose a VPN type that includes 'cisco' when there is no 'l2tp/ipsec'.

3.  Enter the 'server address', 'account name', and any authentication settings you received from your network administrator, 'You can customize the service naming.'.

4.  Click Advanced, click Options, then select the options you want to use:

    -   Send all traffic over VPN connection: Sends all network traffic over the VPN connection, regardless of the network service you use, such as Wi-Fi or Ethernet.

5.  Step was done, Click "Connect"
```