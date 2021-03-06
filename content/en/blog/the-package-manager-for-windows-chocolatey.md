---
author : "Nushan Kodikara"
date : 2020-07-08T17:30:00Z
description : "Automate installations and updates on windows 3rd party softwares"
tags : ["Windows", "Package Manager", "Introduction", "Review"]
title : "The Package Manager for Windows [ Chocolatey ]"
thumbnail: https://unsplash.com/photos/DHYfjAe_eeo/download?ixid=MnwxMjA3fDB8MXxzZWFyY2h8NXx8Y2hvY29sYXRlfHwwfHx8fDE2Mzk1OTEwMjE&force=true&w=640
---
![Chocolatey](/uploads/20200708_224037.jpg "Chocolatey")

## Introduction

Do you ever thought about a single command to install, uninstall or update softwares in Windows? How about a script automatically do everything for you? Guess what, you're in the perfect place!

Chocolatey is a package manager for Windows, which you can install by a single command and do everything with a single command!

#### Showcase

Install softwares

    > choco install vlc

Updated softwares

    > choco upgrade vlc

Uninstall softwares

    > choco uninstall winrar

And explore more in the [docs](https://chocolatey.org/docs "Chocolatey Docs")

### Installation

Step 1

Installation is not much difficulty however, you just need a powershell window with administration Access. Right-click windows icon at bottom left and select powershell with administration Access.

Step 2

Copy the code bellow and paste it in the powershell

    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

And press enter, wait and you're ready to go.

### Usage

**Always start a powershell window with administration Access**. Use the code below to get the help documents

    > choco -?

#### Installing Softwares

Installation is simple and easy as it seams, replace the package name with the software you need to install and you're ready to go!

    > choco install package-name -y

You can also install several softwares at once, for an example I'll install VLC Firefox and Spotify at once as below

    > choco install vlc firefox spotify -y

Also you can get all of the package names and commands by going to [chocolatey](https://chocolatey.org/) site and searching for softwares

![](/uploads/20200708_224814.jpg)

#### Updating softwares

Updating softwares is something harder in Windows, but with chocolatey, harder no more! You can update everything at once by using

    > choco upgrade all -y

Or packages individually by using

    > choco upgrade package-name -y

#### Uninstalling softwares

Usually we need a 3rd party uninstaller for this, but with choco, we are saved! Choco logs and monitors all installation by default so we can easily uninstall anything we install with choco by using

    > choco uninstall package-name -y

### Conclusions

Chocolatey package manager is a very useful tool I use personally on my computers. It makes installations updates and uninstallations easier and less time consuming. However A little bit of knowledge on working with powershell is necessary to operate with chocolatey.