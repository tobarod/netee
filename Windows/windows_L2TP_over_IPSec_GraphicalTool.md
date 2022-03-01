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

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/21.jpg)

```2: Click on Network & Settings.```

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/22.jpg)

```3: Select VPN in the left-hand menu. Then click on Add a VPN connection```

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/23.jpg)

```4: NOTE: Connection name: You can write whatever you want, or VPN. type: L2TP/IPsec with pre-shared key```

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/24.jpg)

```5: Click on Change adapter options```

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/25.jpg)

```6: In the connections list find the connection named in Step 4. Right-click on that connection and select Properties.```

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/26.jpg)

```7: On the Security tab, select Allow these protocols then check the box labeled Microsoft CHAP Version 2 (MS-CHAP v2)```

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/27.png)

> when you want send all traffic over VPN

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/10.png)

```8: Go back to the Network & Internet Settings window and click on the VPN connection. Click the Connect button.```

![Image text](https://github.com/tobarod/netee/blob/main/Img_folder/28.jpg)

## error 1

```bash
无法建立计算机与VPN服务器之间的网络连接，因为远程服务器未响应。这可能是因为未将计算机与远程服务器之间的某种网络设备（如防火墙、NAT、路由器等）配置为允许VPN连接。请与管理员或者服务提供商联系以确定哪种设备可能产生此问题。

The network connection between the computer and the VPN server could not be established because the remote server did not respond. This may be because some network equipment (such as firewall, NAT, router, etc.) between the computer and the remote server is not configured to allow VPN connections. Please contact your administrator or service provider to determine which device may cause this problem.
```

[Reference Repair Method](https://me.jinchuang.org/archives/381.html)

## error 2

```bash
不能建立到远程计算机的连接。你可能需要更改此连接的网络设置。

A connection to the remote computer could not be established. You may need to change the network settings for this connection.
```

**Repair Method**

```bash
此电脑—>右键管理—>设备管理器—>网络适配器—>删除WAN MIniport（ip)—>重启电脑解决。


Right-click the Start button and go to Device Manager.
Expand the Network adapters menu.
Right-click 'WAN MIniport（ip)' and select Uninstall device.
Then,restart computer
```

## error 3

```bash
不能建立到远程计算机的连接，因此用于此连接的端口已关闭。

A connection to the remote computer could not be established, so the port used for this connection is closed.
```

**Repair Method**

```bash
最简单快速的方式是关闭windows防火墙，但是这不安全。
推荐在高级设置中添加出站规则，允许 协议是TCP，端口是 1701和1723
添加操作可以参考
https://jingyan.baidu.com/article/fb48e8bee35d456e622e14b3.html


Can Direct to turn off the Windows Firewall, but this is not secure.
So, Make Sure TCP Port 1723 and 1702 are Allow.
Opening Ports in Windows Firewall

From the Start menu, click Control Panel, click System and Security, and then click Windows Firewall. Control Panel is not configured for 'Category' view, you only need to select Windows Firewall.

Click Advanced Settings.
Click Outbound Rules.
Click New Rule in the Actions window.
Click Rule Type of Port.
Click Next.
On the Protocol and Ports page click TCP.
Select Specific Local Ports and type a value of 1701、1723.
Click Next.
On the Action page click Allow the connection.
Click Next.
On the Profile page click the appropriate options for your environment.
Click Next.
On the Name page enter a name ofReportServer (TCP on port 1701 and 1723)
Click Finish.
Done
```