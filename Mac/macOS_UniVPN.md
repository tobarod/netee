# **Configure UniVPN to use L2TP_over_IPsec or SSL VPN**
**Before you start the configuration**
1. Need to download and install UniVPN software
2. Easy to configure, just import the configuration file prepared by IT and you are ready to use

## Install the UniVPN
### 1.Download and install UniVPN

http://www.leagsoft.com/doc/article/103107.html

Select the UniVPN program that corresponds to the system version you are currently using and download it. 

![image](https://github.com/tobarod/netee/assets/84069016/d46f456b-e8e2-4e5d-b13f-eb5054468bd1)

Open the compressed files of the installer you just downloaded.

![截屏2023-06-21 下午4 21 20](https://github.com/tobarod/netee/assets/84069016/9e3065fe-e7c5-4c1c-9343-3285e5022866)

Run the software installer.

<img width="882" alt="截屏2023-06-21 下午4 31 40" src="https://github.com/tobarod/netee/assets/84069016/84ed2be7-afa1-44fb-9f4f-23dd6c56f1d3">

Since the app was not downloaded through the App store, the app's installer cannot be opened, You will be prompted that the application is from an unknown developer and you will need to approve opening the installer in the Security and Privacy settings in System Preferences.

<img width="532" alt="截屏2023-06-21 下午4 37 02" src="https://github.com/tobarod/netee/assets/84069016/6320c5d5-5164-4d83-ba20-d8ab6a97b7d8">

Open "System Settings" and select "Security and Privacy", then select "Still open" in the "General" option.

![截屏2023-06-21 下午4 16 31](https://github.com/tobarod/netee/assets/84069016/9cdcc422-d3a9-41a2-b214-82ff17442269)

Select "Open" and follow the prompts to complete the installation.

<img width="532" alt="截屏2023-06-21 下午4 17 03" src="https://github.com/tobarod/netee/assets/84069016/17877c01-3804-46dc-a81c-bc14f965fd24">

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
