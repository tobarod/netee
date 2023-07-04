# **Configure UniVPN to use L2TP_over_IPsec or SSL VPN**
**Before you start the configuration**
1. Need to download and install UniVPN software
2. Easy to configure, just import the configuration file prepared by IT and you are ready to use

## Install the UniVPN
### 1.Download and install UniVPN, the application supports Debian and Ubuntu distributions.

http://www.leagsoft.com/doc/article/103107.html

Select the UniVPN program that corresponds to the system version you are currently using and download it. 

![image](https://github.com/tobarod/netee/assets/84069016/00d71b1f-105b-4827-96a6-79ea442632ba)

Open "Terminal" and switch the directory path to the directory where the downloaded file is located, unzip the file and run the installation file.

```bash
cd /home/bot/Download
unzip univpn-linux-64-10781.13.0.0522.zip
cd univpn-linux-64-10781.13.0.0522
chmod +x univpn-linux-64-10781.13.0.0522.run
sudo ./univpn-linux-64-10781.13.0.0522.run

```

### 2.Import configuration files

Download and unzip the "VPN Profile" zip file. 

vpn profile download link：https://github.com/tobarod/netee/raw/main/VPN_Profiles/VPN_Profiles.zip

Run UniVPN and click on "New Connection"

![image](https://github.com/tobarod/netee/assets/84069016/70c7efcb-bbaf-4318-acc9-4d15921f331b)

Locate the unzipped folder of the "VPN profile". Import the downloaded configuration file.

PS: The downloaded VPN profile contains L2TP VPN and SSL VPN, which can be used on an as-needed basis.

![image](https://github.com/tobarod/netee/assets/84069016/48039472-d039-4796-bd84-b9ab546ac000)

## 登录VPN账户
### 中文
请使用统一身份认证的用户名和密码登录 VPN。 

统一身份认证的用户名由邮箱账户的用户名部分加上统一身份认证服务的域名部分组成。详情请见下文示例部分。

示例

如您的邮箱账户用户名是：xiaoming.zhang@dorabot.com

则您的统一身份认证用户名为：xiaoming.zhang@dorabot.xyz

第一次使用统一身份认证服务时，请在公司内网中访问统一身份认证账户管理页面，修改账户初始密码以激活帐户。

统一身份认证账户管理页面：http://password.dorabot.xyz/RDWeb/Pages/zh-CN/password.aspx （需在公司内网访问，或连接内网 VPN 后访问）


### English
Please log in to the VPN using your Unified Identity Authentication username and password.

The username for Unified Identity Authentication consists of the username portion of the email account plus the domain name portion of the Unified Identity Authentication service. Please see the example section below for more details. 

Example

If your email account username is: james.smith@dorabot.com

Then your Unified Identity Authentication user name is: james.smith@dorabot.xyz

When using the Unified Identity Authentication service for the first time, please visit the Unified Authentication account management page in the company intranet and change the initial account password to activate the account.

Unified Identity Authentication account management page: http://password.dorabot.xyz/RDWeb/Pages/zh-CN/password.aspx (must be accessed from the company intranet, or after connecting to the intranet VPN)
