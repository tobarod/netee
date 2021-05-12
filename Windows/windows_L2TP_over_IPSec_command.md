# Configuration L2TP over IPSec VPN by command

```Network administrator will provide you with information```

```txt
Type VPN : L2TP over IPSec
Server address : XXX
Account Name :XXX
password : XXX
Shared Secret: XXXX
```

```step 1: open powershell of admin```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/60.png)

```step 2: Modify your own script from the template```

```bash
Add-VpnConnection -Name "XXX-Customize by yourself" -ServerAddress "XXX-server address" -TunnelType "L2tp" -EncryptionLevel "Maximum" -AuthenticationMethod Chap,MSChapv2 -SplitTunneling -AllUserConnection -L2tpPsk "XXX-Shared secret" -Force -RememberCredential -PassThru
```

```step 3: ```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/61.png)

> when you want send all traffic over VPN

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/10.png)

```step 4: Done and go connect```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/62.png)

