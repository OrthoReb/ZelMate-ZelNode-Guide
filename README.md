***

<p align="center">
  <img width="860" height="315" src="https://imgur.com/tQQkMPn.png/860/315">
</p>

***

**This guide will assist you in setting up a ZelNode on a DigitalOcean VPS running Ubuntu 18.04.5 x 64**

**If you require further assistance contact the support team on [Discord](https://discord.gg/szN9yZ) or [Telegram English](http://t.me/zelcash) / [Chinese](http://t.me/zelcashcn) / [Russian](http://t.me/zelcashru)**
***
## Requirements
1) **ZEL collateral (10K Basic / 25K Super / 100K BAMF)**
2) **Control wallet (ZelMate)**
3) **VPS running Linux Ubuntu 18.04 (benchmark requirements can't be guaranteed for servers the team hasn't tested)**
4) **SSH client such as [Putty](https://www.putty.org/) or [MobaXterm](https://mobaxterm.mobatek.net/download.html)**
***
## Contents
* **Section A : Downloading ZelMate Wallet**
* **Section B : Creating [DigitalOCean](https://www.digitalocean.com/) VPS**
* **Section C : Downloading and Installing [Putty](https://www.putty.org/)**
* **Section D : Connecting VPS and Installing ZelNode Script**
* **Section E : Connecting and Starting ZelNode**

***

## Section A: Downloading ZelMate Wallet
**(Make sure to backup your wallet.dat file for previous ZelCore full nodes or Swing wallets)**

***Step 1***
* **Download the current ZelMate wallet based on your OS by clicking [here](https://github.com/zelcash/zelcash-swing-wallet/releases)**

![Example-OS](https://imgur.com/0bIBc4y.png)

***

***Step 2***
* **First time users of a ZEL full node need to download the bootstrap file to decrease sync time by clicking [here](https://github.com/zelcash/zelcash/wiki/Bootstrap-for-ZelNodes)**

![Example-OS](https://imgur.com/wYChNI6.png)

***

***Proceed to the next section while ZelMate wallet is downloading the blockchain***

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
* **Paste the password into the Putty terminal by right clicking (it will not show the password just press enter)**

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

* **Go to 'Own Addresses' tab, and select 'New T (Transparent) Address' button to create a new address**

![Example-installing](https://imgur.com/MwQ6sZN.png)
***

***Step 2 (ZelMate)*** 

* **Name new address, `zelNodeBasic1` is just an example (optional)**

![Example-installing](https://imgur.com/snfDHth.png)
***

***Step 3 (ZelMate)*** 

* **Fund that address with EXACT amount in a SINGLE TRANSACTION (10k Basic / 25k Super / 100k BAMF)**

![Example-installing](https://imgur.com/mneX1dm.png)
***

***MAKE MULTIPLE BACKUPS OF YOUR WALLET.DAT AND PRIVATE KEYS, DO THIS FOR EVERY NEW ADDRESS THAT IS GENERATED***

***(CLICK 'WALLET' TAB AND SELECT 'BACKUP' FOR WALLET.DAT AND 'EXPORT PRIVATE KEYS' FOR PKS)***

***

***Step 4 (ZelMate)*** 

* **Select 'New ZelNode' under the 'ZelNodes' tab**

![Example-installing](https://imgur.com/1fJcBCR.png)
***

***Step 5 (ZelMate)*** 

* **Add your ZelNode information to the Create ZelNode popup and click 'Save' (Open up a Notepad file)**  

![Example-installing](https://imgur.com/RiJtpsd.png)

* **ZelNode Alias - Can name the ZelNode anything you like (E.g.: trial123Basic1)**
* **Address (IP:Port Number) - The IP address & port (16125) of your ZelNode VPS/server**
* **ZelNode Key - ZelMate will auto-populate this field**
* **ZelNode Output - ZelMate will automatically populate the dropdown with transactions that match the collateral for an address (E.g. after you send EXACTLY 10,000 Zel to an address for a Basic, etc.). ZelNode Address and ZelNode Amount will auto-populate so you can ensure you chose the correct ZelNode Output for the ZelNode tier you want to set up.**
* **Copy the ZelNode Key into Notepad for use later when setting up ZelNode VPS/server**

***

***Step 6 (ZelMate)***

* **ZELmate will display a message that your ZelNode was added and the zelnode.conf file and that the wallet needs to be restarted and reindexed if its your first node**

* **Press "Yes" to quit and restart ZELmate. Let the wallet launch and sync completely**


***

***Step 7 (VPS)***

* **Log back into your VPS with the new username and password from Section D: Steps 9 and 10**

***

***DO NOT RUN THE INSTALL SCRIPT AS ROOT, ONLY RUN IT AS THE NEW USER THAT WAS MADE IN STEP 9***

***

***Step 8 (VPS)***

* **Paste the code below into the Putty terminal then press enter**

`wget -O zelnode.sh https://raw.githubusercontent.com/zelcash/ZelNodeInstallv3/master/zelnodev3.sh && chmod +x zelnode.sh && ./zelnode.sh`

***

***HUGE SHOUTOUT TO GOOSE, SKYSLAYER AND DK808 FOR PUTTING TOGETHER THIS INSTALL SCRIPT***

***

***Step 9  (VPS)***

* **Confirm IP and enter private key from Step 3**

![Example-installing](https://i.imgur.com/TFMP41b.jpg.png)
***

***Step 10***

* **Go to the ZelCash block explorer** 

`https://explorer.zel.cash/`

![Example-installing](https://imgur.com/liBNF5O.png)
***

***Step 11 (VPS)***

* **Press any key, then CTRL-C when the blocks match explorer in Step 6**

![Example-installing](https://i.imgur.com/46H4YJn.jpg.png)

![Example-installing](https://imgur.com/CqD1Kqa.png)
***

**(WAIT AT LEAST 15 MINUTES AFTER THE THE BLOCKCHAIN IS DONE SYNCING BEFORE PROCEEDING TO THE NEXT STEP)**

***Step 12 (ZelMate)*** 

* **Once everything is ready to activate, Click the ZelNodes tab, on the left field, find the ZelNode you wish to start, right click, and select Start ZelNode**

![Example-installing](https://imgur.com/es0V20X.png)

***

***Step 13***

* **Run the following command in VPS to confirm that your ZelNode is showing 'Status 4' (If VPS does not show successfully started, wait 5 minutes and run the command again. Repeat if necesary)**

`zelcash-cli getzelnodestatus`

![Example-installing](https://imgur.com/nj76J7D.png)

* **You can also view your ZelNode on the block explorer `https://explorer.zel.cash/zelnodes`**

![Example-installing](https://imgur.com/SkGqa6D.png)

**(It will show up as 'PRE_ENABLED' prior to 15 confirmations)**

***

***CONGRATULATIONS AND THANK YOU FOR BEING A PART OF THE COMMUNITY!!!!!!!!!!!!!***

***
