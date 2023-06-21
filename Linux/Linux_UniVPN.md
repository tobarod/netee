# **Configure UniVPN to use L2TP_over_IPsec or SSL VPN**
**Before you start the configuration**
1. Need to download and install UniVPN software
2. Easy to configure, just import the configuration file prepared by IT and you are ready to use

## Install the UniVPN
### 1.Download and install UniVPN

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
