***

<p align="center">
  <img width="860" height="315" src="https://imgur.com/tQQkMPn.png/860/315">
</p>

***

**This guide will assist you in setting up a ZelNode on a DigitalOcean VPS running Ubuntu 18.04.5 x 64**

**If you require further assistance contact the support team on [Discord](https://discord.gg/szN9yZ) or [Telegram English](http://t.me/zelcash) / [Chinese](http://t.me/zelcashcn) / [Russian](http://t.me/zelcashru)**
***
## Requirements
1) **ZEL Collateral (10K Basic / 25K Super / 100K BAMF)**
2) **Controller wallet (ZelMate Swing Wallet)**
3) **VPS running Linux Ubuntu 18.04 (benchmark requirements can't be guaranteed for servers that the team hasn't tested)**
4) **SSH client such as [Putty](https://www.putty.org/)**
***
## Contents
* **Section A : Preparing ZelMate Wallet**
* **Section B : Creating [DigitalOCean](https://www.digitalocean.com/) VPS**
* **Section C : Downloading and Installing [Putty](https://www.putty.org/)**
* **Section D : Connecting VPS and Installing ZelNode Script**
* **Section E : Connecting and Starting ZelNode**

***

## Section A: Downloading ZelMate Wallet
**(Make sure to backup your wallet.dat file for previous ZelCore full nodes or Swing wallets)**

***Step 1***
* **Download the current ZelCore wallet based on your OS by clicking [here](https://zelcore.io/#download)**

![Example-OS](https://imgur.com/0bIBc4y.png)

***

***Step 2***
* **First time users of a ZEL full node need to download the bootstrap file to decrease sync time by clicking [here](https://github.com/zelcash/zelcash/wiki/Bootstrap-for-ZelNodes)**

***

***Proceed to the next section while ZelMatee wallet is syncing the blockchain***

***

## Section B: Creating DigitalOcean VPS
***Step 1***
* **Register at [DigitalOcean](https://m.do.co/c/c9c22684c5db) (use this [referral link](https://m.do.co/c/c9c22684c5db) to receive a $100 credit that's good for 2 months)**

***

***Step 2***
* **After you have your account setup go [here](https://cloud.digitalocean.com/droplets?i=8fe2ca&preserveScrollPosition=false) to create your ZelNode droplet**

![Example-OS](https://imgur.com/WYFdC1j.png)

***

***Step 3***
* **Choose server type: 'Ubuntu 18.04'**
![Example-OS](https://imgur.com/4hM9ugU.png)

***

***Step 4***
* **Choose Droplet (Basic/Super/BAMF)**

![Example-OS](https://imgur.com/sVaawzt.png) ![Example-OS](https://imgur.com/1hAuT2T.png) ![Example-OS](https://imgur.com/Yc3Wm7q.png)

***

***Step 5***

![Example-Location](https://imgur.com/hjmZiaf.png)

**(Consider choosing a data center not near you to help decentralize the network. The location of the data center does not affect your rewards or setup process.)**

***

***Step 6***

![Example-OS](https://imgur.com/qlYDSVn.png)

***


## Section C: Downloading and Installing Putty

***Step 1***
* **Download Putty [here](https://www.putty.org/)**

***

***Step 2***
* **Select the correct installer depending upon your operating system, and follow the install instructions** 

![Example-Putty Installer](https://imgur.com/U7eaNSh.png)

***

## Section D: Connecting VPS and Installing ZelNode Script

***Step 1***
* **Copy your VPS IP (located within Droplets tab)**
![Example-DO](https://imgur.com/8YWMNxW.png)

***

***Step 2***
* **Open the Putty terminal and fill in the "Host Name" box with the IP address of your VPS**

![Example-PuttyLogin](https://imgur.com/gMkd6fs.png)

***

***Step 3***
* **Once you hit 'Open' a security alert will open up (click yes)**

![Example-RootPassEnter](https://imgur.com/z0N2AMT.png)

***

***Step 4***
* **Type "root" as the login/username**

![Example-Root](https://imgur.com/DumQVJ5.png)

***

***Step 5***
* **Copy the root password that DigitalOcean emailed you**

***

***Step 6*** 
* **Paste the password into the Putty terminal by right clicking (it will not show the password so just press enter)**

![Example-RootPassEnter](https://imgur.com/TqeHV2C.png)

***

***Step 7*** 
* **Enter password for root (UNIX password same as Step 5)**

* **Make new password and confirm**

![Example-RootPassEnter](https://imgur.com/vSXtaaG.png)

***

***Step 8*** 
* **Update VPS with the following 2 commands**

`sudo apt-get update`

`sudo apt-get upgrade -y`

***

***Step 9***
* **Adduser to secure your VPS, by adding a new username so you aren't running everything as root**  

* **Run the command below and use a username that you want associated with this server ('whodatbamf1' is an example, you need to generate your own username)** 

`adduser YOURUSERNAME`

![Example-Bash](https://imgur.com/HJwb8tT.png)

***

***Step 10***

* **You will then need to make a new password associated with your new username.  Hit 'Enter' for the next 5 lines after your new password has been set, then 'Y' to save your information.**

![Example-Bash](https://imgur.com/suf0D9Y.png)

***

***Step 11***

* **Grant sudo permissions for your adduser by running the command below to activate it**

`usermod -aG sudo YOURUSERNAME`

***

***Step 12***

* **Reboot server with the following command**

`sudo reboot -n`

* **Close Putty terminal while server reboots**

***

## Section E : Connecting and Starting ZelNode (ZelMate and VPS)

***Step 1 (ZelMate)*** 

* **Go to Own Addresses tab, and select New T (Transparent) Address button to create a new address. **

![Example-installing](https://camo.githubusercontent.com/4cfe66595232ddb2a18195b51570b318ca66b4d6/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f3430363535383431373338363437313432342f3534313736313234343830363531323636312f6e65775f616464726573732e504e47.png)
***

***Step 2 (ZelCore)*** 

* **Name your ZelNode**

![Example-installing](https://imgur.com/YspTi4J.png)
***

***Step 3 (ZelCore)*** 

* **Save your private key that is generated in ZelCore and enter on VPS when prompted**  

![Example-installing](https://imgur.com/It7FQjW.png)
***

***Step 4 (VPS)***

* **Log back into your VPS with the new username and password from Section D: Steps 9 and 10**

***

***DO NOT RUN THE INSTALL SCRIPT AS ROOT, ONLY RUN IT AS THE NEW USER THAT WAS MADE IN STEP 9!!!!!!!!!!!!!!!***

***

***Step 5 (VPS)***

* **Paste the code below into the Putty terminal then press enter**

`wget -O zelnode.sh https://raw.githubusercontent.com/zelcash/ZelNodeInstallv3/master/zelnodev3.sh && chmod +x zelnode.sh && ./zelnode.sh`

***

***HUGE SHOUTOUT TO GOOSE, SKYSLAYER AND DK808 FOR PUTTING TOGETHER THIS INSTALL SCRIPT***

***

***Step 6  (VPS)***

* **Confirm IP and enter private key from Step 3**

![Example-installing](https://i.imgur.com/TFMP41b.jpg.png)
***

***Step 7***

* **Go to the ZelCash block explorer** 

`https://explorer.zel.cash/`

![Example-installing](https://imgur.com/liBNF5O.png)
***

***Step 8 (VPS)***

* **Press any key, then CTRL-C when the blocks match explorer in Step 6**

![Example-installing](https://i.imgur.com/46H4YJn.jpg.png)

![Example-installing](https://imgur.com/CqD1Kqa.png)
***

***Step 9 (ZelCore)*** 

* **Activate your ZelNode**

![Example-installing](https://imgur.com/xyPmofR.png)

* **Successfully started will show if everything is done properly ('startzelnode local false' isn't needed)**

![Example-installing](https://imgur.com/GGpcyFA.png)

***(It will take 15 confirmations for your ZelNode to show up in 'MY ZELNODES')***
***

***Step 10***

* **Run the following command in VPS to confirm that your ZelNode is showing 'Status 4' (If VPS does not show successfully started, wait 5 minutes and run the command again. Repeat if necesary)**

`zelcash-cli getzelnodestatus`

![Example-installing](https://imgur.com/nj76J7D.png)

* **You can also view your ZelNode on the block explorer `https://explorer.zel.cash/zelnodes`**

![Example-installing](https://imgur.com/SkGqa6D.png)

**(It will show up as 'PRE_ENABLED' prior to 15 confirmations)**

***

***CONGRATULATIONS AND THANK YOU FOR BEING A PART OF THE COMMUNITY!!!!!!!!!!!!!***

***
