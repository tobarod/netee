# **配置 UniVPN 客户端 / Configure the UniVPN client**
**开始配置前的说明 / Before you start the configuration**
1. 需要下载并安装 UniVPN 软件 / Need to download and install UniVPN software
2. 配置简单，只需导入 IT 部门准备的配置文件即可使用 / Easy to configure, just import the configuration file prepared by IT and you are ready to use

## 安装 UniVPN / Install the UniVPN
### 1. 下载并安装 UniVPN / Download and install UniVPN

[UniVPN Linux 客户端下载链接 / UniVPN Linux client download link](https://download.leagsoft.com/download/UniVPN/linux/univpn-linux-64-10781.15.0.1208.zip)

打开 "终端"，将目录路径切换到下载文件所在的目录，解压文件并运行安装文件。 / Open "Terminal" and switch the directory path to the directory where the downloaded file is located, unzip the file and run the installation file.

```bash
cd /home/bot/Download
unzip univpn-linux-64-10781.13.0.0522.zip
cd univpn-linux-64-10781.13.0.0522
chmod +x univpn-linux-64-10781.13.0.0522.run
sudo ./univpn-linux-64-10781.13.0.0522.run

```

### 2. 导入配置文件 / Import configuration files

下载并解压 "VPN 配置文件 "压缩文件。 / Download and unzip the "VPN Profile" zip file. 

VPN 配置文件下载链接 / vpn profile download link：https://github.com/tobarod/netee/raw/main/VPN_Profiles/VPN_Profiles.zip

运行 UniVPN 并点击 "新建连接"。 / Run UniVPN and click on "New Connection"

![image](https://github.com/tobarod/netee/assets/84069016/70c7efcb-bbaf-4318-acc9-4d15921f331b)

找到解压后的 "VPN 配置文件 "文件夹。导入下载的配置文件。 / Locate the unzipped folder of the "VPN profile". Import the downloaded configuration file.

提示: 下载的 VPN 配置文件包含 L2TP VPN 和 SSL VPN，可根据需要使用。 / PS: The downloaded VPN profile contains L2TP VPN and SSL VPN, which can be used on an as-needed basis.

![image](https://github.com/tobarod/netee/assets/84069016/48039472-d039-4796-bd84-b9ab546ac000)

## 登录VPN账户
### 中文
请使用统一身份认证的用户名和密码登录 VPN。 

统一身份认证的用户名由邮箱账户的用户名部分加上统一身份认证服务的域名部分组成。详情请见下文示例部分。

示例

如您的邮箱账户用户名是：xiaoming.zhang@dorabot.com

则您的统一身份认证用户名为：xiaoming.zhang@dorabot.xyz

第一次使用统一身份认证服务时，请先阅读企业微信的工作台 “Dorabot 公共服务” 页面中的 “统一身份认证系统” 说明文档，并在公司内网中访问统一身份认证账户管理页面，修改账户初始密码以激活帐户。

统一身份认证账户管理页面：http://password.dorabot.xyz/RDWeb/Pages/zh-CN/password.aspx （需在公司内网访问，或连接内网 VPN 后访问）


### English
Please log in to the VPN using your Unified Identity Authentication username and password.

The username for Unified Identity Authentication consists of the username portion of the email account plus the domain name portion of the Unified Identity Authentication service. Please see the example section below for more details. 

Example

If your email account username is: james.smith@dorabot.com

Then your Unified Identity Authentication user name is: james.smith@dorabot.xyz

When using the Unified Identity Authentication service for the first time, please read the "Unified Identity Authentication System" instruction document on the "Dorabot Public Services" page of the Enterprise Wechat （WeCom） workbench, and visit the Unified Identity Authentication Account Management page in the company intranet and change the initial account password to activate the account. 

Unified Identity Authentication account management page: http://password.dorabot.xyz/RDWeb/Pages/zh-CN/password.aspx (must be accessed from the company intranet, or after connecting to the intranet VPN)
