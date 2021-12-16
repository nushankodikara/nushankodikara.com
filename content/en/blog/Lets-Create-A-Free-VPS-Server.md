---
author: "Nushan Kodikara"
title: "Let's Create a Free VPS Server"
description: "The best way to get started with VPS is to create a free VPS server. This article will help you to through the journey."
date: 2021-12-16T08:32:21+05:30
tags: ["VPS", "Free To Go"]
thumbnail: https://unsplash.com/photos/M5tzZtFCOfs/download?ixid=MnwxMjA3fDB8MXxzZWFyY2h8MXx8c2VydmVyfHwwfHx8fDE2Mzk1NjQ4NTg&force=true&w=640
draft: false
---

The process of creating a free VPS server is very simple. Some people overcomplicate the process and the ones who follow them will get frustrated. Let's see how we can create a free VPS server in just a few steps, without complicating the process. If you got any issues while following the steps, please feel free to contact me through [Telegram](https://t.me/+FtAyOh8JBWg4OGU1).

## Step 1: Creating An Account On VPS Provider

Today in this guide, we're using a site called [Hax.co.id](https://hax.co.id/). It's a site that provides free VPS servers. Unfortunately, this site doesn't provide any premium servers, in-case you needed to upgrade. So, if you need to create a premium server, you can use [DigitalOcean](https://www.digitalocean.com/). Follow along the steps below to create an account on the site.

Browse to the site [https://Hax.co.id/](https://hax.co.id/).

![Homepage](/uploads/2021_12_16_P1.png)

You will be greeted with this home page. If you're a new user, you need to click on the button `Register` to create an account. Remember, you need an Telegram account to create an account on this site. After clicking on the register button, you will be redirected to the registration page, where you'll be asked for your telegram ID.

![Register](/uploads/2021_12_16_P2.0.png)

Here enter your telegram ID. If you don't know your telegram ID, just go to the telegram app and search for @haxTG_bot.

![Telegram Search](/uploads/2021_12_16_P2.1.png)

Click on the first result and you'll get to the telegram bot page, tap on `start` button and the bot will send you your telegram ID.

![Telegram Bot](/uploads/2021_12_16_P2.3.png)

Enter Your Telegram ID in the form and click on the `Submit` button. As soon as you tapped on the submit button, The bot will send you an Authentication Code. Copy this code and enter it in the next form, and click submit.

![Authentication Code](/uploads/2021_12_16_P2.4.png)
![Registration Forum](/uploads/2021_12_16_P3.png)

Congratulation! You have successfully registered on the site. Now, you can login to your account.

![Login](/uploads/2021_12_16_P4.png)

## Step 2: Creating A VPS Server

After logging in to the site, you'll be greeted by the VPS information page. where you can see that you do not have a VPS server yet. Click on the `Create one here` button to create a VPS server.

![Create VPS Server](/uploads/2021_12_16_P5.png)

After clicking on the button, you'll be redirected to the VPS creation page. Here you can setup your VPS server.

![VPS Creation](/uploads/2021_12_16_P6.png)

Let's go through the forum to setup your VPS server.

-   First you need to select your Data Center. Select any data center from the dropdown menu.

-   Next you need to select your Operating system. I have choosed Ubuntu 20, Choose your system according to your needs. If you don't know what is the best one for you, just go with Ubuntu 20.

-   Next you need to enter a SSH password. This password will be used when we connect to your VPS server through SSH. Remebmer to keep this password safe!

-   This site requires you to select the purpose of your VPS, select one according to your needs.

-   Tick all the tick boxes with license agreements and click on `Create VPS` button to complete your VPS creation.

![VPS Created!](/uploads/2021_12_16_P7.png)

Congratulations! you have succesfully created your VPS server. Now, you can access your VPS server through SSH. But before that, you need to setup a domain name for easy access.

## Step 3: Creating A Domain Name

I have written a guide on how to create your own free Top level domain using Freenom and how you can connect it to a free DNS service before. [goto This This Link](https://www.nushankodikara.com/blog/free-top-level-domain-names-2020/) And follow the steps to create and cofigure a domain name.

## Step 4: Configuring The DNS Server

After creating your domain name, you need to configure your DNS server. This is the place where you can add your VPS IP to your DNS server. First go to your VPS server's [Information page](https://hax.co.id/vps-info/).

![VPS Information](/uploads/2021_12_16_P8.png)

Here you can see your IPV6 Address. Copy this IPV6 address and come to your DNS settings on netlify ( Configured in Step 3 ).

![DNS Settings](/uploads/2021_12_16_P9.png)

Click on `Add new record` button and enter the following details.

![DNS Record](/uploads/2021_12_16_P10.png)

Your Record Type Must be `AAAA` which stands for IPV6 aliases. in the Name tab enter `@` symbol to indicate you're using the root domain. In the Value tab enter your IPV6 address, which you copied from the server. And press save to save your record.

![DNS Record](/uploads/2021_12_16_P11.png)

If you did it correctly you'll be able to see your DNS record as in the above image.

## Step 5: SSH Access

Now here comes the fun part. Connecting to your VPS server. Here you have 2 methods.

### Method 1: Web Base Terminal

Go to your VPS server's [Information page](https://hax.co.id/vps-info/) again. and click on the `Web Base Terminal` link at the bottom of the information box.

![Web Base Terminal](/uploads/2021_12_16_P12.0.png)

Then you'll be redirected to the terminal page. Here first you need to enter your SSH password, which we created in step 2. Press on connect button and you'll be connected to your VPS server.

![SSH Connected!](/uploads/2021_12_16_P12.1.png)

### Method 2: SSH Terminal (Recommended)

This method is same for all Windows, Mac And linux desktops as well as android terminals.

If you're in windows. open Command Prompt (CMD), If you're in Linux or Mac, Open up a terminal window. If you're using an android device you can download and use an app called [Termius](https://play.google.com/store/apps/details?id=com.server.auditor.ssh.client). And follow along!

First start a CMD or Terminal window.

![Terminal](/uploads/2021_12_16_P12.3.png)

Now Enter the following Command And press Enter.

```terminal
ssh root@<yourdomain>
```

Here replace `<yourdomain>` with the domain name you registered in step 3.

![SSH Command](/uploads/2021_12_16_P13.png)

After pressing enter, if you followed all the above steps correctly, you should be able to see a prompt asking `Are you sure you want to continue connecting (yes/no/[fingerprint])?`. You need to enter `yes` and press enter button to continue.

![SSH Command](/uploads/2021_12_16_P14.png)

Again you'll be asked for the SSH password we created in step 2. Enter it and press enter. (Please note you won't be able to see the password in the terminal window while entering it. It's for security purposes.)

![SSH Command](/uploads/2021_12_16_P15.png)

If you did everything correctly, you should be able to see your VPS server's terminal.

![SSH Terminal](/uploads/2021_12_16_P16.png)

Congratulations! You have successfully connected to your VPS server. Now, you can access your VPS server through SSH.

## Step 6: Uploading Your VPS Server

Technically you can do whatever you need right now. But I would recommend you to update your VPS server to the latest version. Follow along the guide to do so.

First enter the command

```terminal
sudo apt-get update
```

Then press enter to start updating your repositories.

![Update Repositories](/uploads/2021_12_16_P17.png)

It would take a minute or two to update your repositories. After updating your repositories, you need to upgrade your installed packages. to do so, enter the command

```terminal
sudo apt-get upgrade
```

Then press enter.

![Update Packages](/uploads/2021_12_16_P18.png)

Here you'll be asked again to confirm your upgrade. Enter `y` and press the enter button to allow the upgrade.

![Update Packages](/uploads/2021_12_16_P19.png)

This will take a while to complete so stay tight. While upgrading your packages, you'll see a prompt like this one.

![Update Packages](/uploads/2021_12_16_P20.png)

Here navigate with up and down arrow keys and select the option which say `keep the local version currently installed`. Then press enter to confirm. Let the process run. Finally you'll be able to see a done message.

![Update Packages](/uploads/2021_12_16_P21.png)

Congratulations! You have successfully updated your VPS server.

We'll explore what we can do with such a server in the next article. Follow me on TikTok to get an quick update over the next few days.
