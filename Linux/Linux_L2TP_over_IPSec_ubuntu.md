# Using L2TP in Ubuntu operates as follows。
```The network administrator will provide you with information```

```txt
Type VPN : L2TP over IPSec
Server address : 123.123.123.123 (Replace 123.123.123.123 in the configuration file with your server address)
Account Name :XXX
password : XXX
Shared Secret: XXXX
```
```1：Open terminal```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/41.png)

```2：Enter the following command line by line in the terminal.```
```txt
sudo add-apt-repository ppa:nm-l2tp/network-manager-l2tp
sudo apt-get update
sudo apt-get install network-manager-l2tp-gnome
```
```3：Some of the parameters you will use later,User name, user password and PSK(Pre-shared key) are issued by the IT team. Remember to apply for L2TP permission before use.```
```txt
Gateway:123.123.123.123
Phase1 Algorithms: aes256-sha256-modp2048
Phase2 Algorithms: aes256-sha256
```
```4：Then follow the steps on the picture to set it step by step.```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/42.png)

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/43.png)

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/44.png)

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/45.png)

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/46.png)