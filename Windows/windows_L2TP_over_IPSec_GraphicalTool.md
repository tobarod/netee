# Configuration L2TP over IPSec VPN by Graphical tool

```Network administrator will provide you with information```

```txt
Type VPN : L2TP over IPSec
Server address : XXX
Account Name :XXX
Password : XXX
Shared Secret: XXXX
```

```1: Click the Start button in the bottom-left corner of the screen. Click on Settings.```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/21.jpg)

```2: Click on Network & Settings.```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/22.jpg)

```3: Select VPN in the left-hand menu. Then click on Add a VPN connection```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/23.jpg)

```4: NOTE: Connection name: You can write whatever you want, or VPN. type: L2TP/IPsec with pre-shared key```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/24.jpg)

```5: Click on Change adapter options```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/25.jpg)

```6: In the connections list find the connection named in Step 4. Right-click on that connection and select Properties.```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/26.jpg)

```7: On the Security tab, select Allow these protocols then check the box labeled Microsoft CHAP Version 2 (MS-CHAP v2)```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/27.png)

> when you want send all traffic over VPN

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/10.png)

```8: Go back to the Network & Internet Settings window and click on the VPN connection. Click the Connect button.```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/28.jpg)

## error 1

```bash
无法建立计算机与VPN服务器之间的网络连接，因为远程服务器未响应。这可能是因为未将计算机与远程服务器之间的某种网络设备（如防火墙、NAT、路由器等）配置为允许VPN连接。请与管理员或者服务提供商联系以确定哪种设备可能产生此问题。

The network connection between the computer and the VPN server could not be established because the remote server did not respond. This may be because some network equipment (such as firewall, NAT, router, etc.) between the computer and the remote server is not configured to allow VPN connections. Please contact your administrator or service provider to determine which device may cause this problem.
```

[Reference Repair Method](https://me.jinchuang.org/archives/381.html)