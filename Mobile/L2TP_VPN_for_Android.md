# Configuration L2TP over IPSec VPN by Settings

## Android 12 or higher
**Please note for users with system version Android 12 or higher.**

```txt
In Android 12 both IPsec Xauth and L2TP were removed completly.
The only available authentication types of the android vpn built-in client are:
IKEv2/IPsec MSCHAPv2
IKEv2/IPSec PSK
IKEv2/IPSec RSA

so, if your device were Android version 12, please add SSL VPN, don't add this L2TP VPN.
```
[SSL VPN for Android or iOS](https://github.com/tobarod/netee/blob/main/Mobile/SSL_VPN_for_Android_or_iOS.md)

## Android 11 or lower

```Network administrator will provide you with information```

```txt
Type VPN : L2TP over IPSec
Server address : XXX
Account Name :XXX
Password : XXX
Shared Secret: XXXX
```

```step 1: find and enter Settings```

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/70.png)

```step 2: Search VPN by search function, then Add VPN network```

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/71.jpg)

```step 3: How to turn VPN ON and OFF```

```bash
# how to
Settings --> Other networks and connections --> VPN --> Select and connect or disconnect

# verify status
Normally, the VPN icon is displayed at the top of the screen

# if failure, please keep a screenshot of the error and contact the administrator
```
