---
layout: post
title:  "ownCloud Quickstart Guide"
date:   2019-02-20 15:40:15 +0000
categories: 
---

## Introduction
The purpose of this document is to guide users through the installation of ownCloud server, adding users and accessing the ownCloud server using a client application in a short timeframe.  This document is written specifically for installation on an Apple Mac running OSX High Sierra version 10.13.6 or higher.  Note that this document details an installation for demonstration purposes only.  This method must not be used for a production installation.

## What is ownCloud?
ownCloud allows individual users and enterprise organisations to host their documents within a on-premise, secure cloud infrastructure that is entirely within the owners control.  In terms of architecture, the software utilises a client-server modal, where documents and other software assets are stored on servers and can be accessed through multiple client applications. 

## Installed Prerequisites
This guide covers the installation of the ownCloud server software on a virtualbox instance as  this allows a simple and quick installation for demonstration purposes.  Virtualbox version 5.2.26 for OSX is available [here](https://download.virtualbox.org/virtualbox/6.0.4/VirtualBox-6.0.4-128413-OSX.dmg).

## Method
# Installation of ownCloud server
1. Obtain an image to run on virtualBox.  Open [https://owncloud.com/download/](https://owncloud.com/download/) in your browser and download the image by clicking the "DOWNLOAD" button in the "Download ownCloud Server" section.  You will be expected to register with ownCloud at this stage in the process.  Enter your details, making sure that you submit a **valid email address** (this will be used to send your license to) and also ensure that the Download version that you select is the _ownCloud Server Appliance (VirtualBox)_ version.

2. When the image has downloaded, launch virtualBox and select *File* - *Import Appliance*.  Click on the folder icon and browser to select your image.  Click *Continue* to proceed to the *Appliance Settings* screen.

3. Leave the settings at their defaults and press *Import*.

4. Press *Agree* to agree to the terms and conditions of the image license agreement and the import will commence.

5. When the import has completed, select the *UCS 4.3-with-ownCloud* image in the left hand column in virtualBox and press *Start*.  The server will present 3 options.  Allow the boot process to proceed with the *start owncloud* option by default.

6. As this is a first installation, you will be asked several questions for configuration purposes.  Enter your preferred to language and city and click *NEXT*

7. In the *Domain and network configuration* section, make sure that *Obtain IP address automatically (DHCP)* box is checked, leave the remaning field with their default values.  Note the value of the *IPv4/IPv6 address* and click *NEXT*

8. A warning message will appear listing servers that cannot be reached.  These will be configured later so, for the moment, press *Continue without access to the repository servers*

9. For the *domain setup*, leave the *Manage users and permissions directly on the system* option selected and click *NEXT*.

10. In the *Account Information* section, enter your organisation name, a valid email address and a strong password.

11. In the *Host Settings* section, leave the default values and click *NEXT*.

12.  You are all set.  Click on *Configure System* and, when the setup has completed, click *FINISH*.

The server has now been installed.  Proceed immediately to the next step

# Setting up ownCloud server
Start up a session in your web browser and navigate to the ip address that was set up in step 7 of the previous section.  This address will also be displayed just after the server has been installed.  i.e.

![server start](../../../../images/server_start.png)

You will be asked to activate your license, which will have been sent to you, by email, in a ucs.license file when you originally registered with ownCloud (see step 1 of the *Installation of ownCloud server* section).  Check your inbox for the email and detach the license file in a secure location.

Click on *Upload Licence Data* and then click on *FINISH* when the "Activation Successful" message is displayed.  You will now be directed to the welcome screen.  Take note of the administrator username and password that is displayed there.  You may also be asked a couple of survey questions.  Answer them as you see fit and click finish.

# Adding a user account
1. On the main screen, click on the *Users* block.  You will be brought to the *Users* section which will list one user (Administrator)
2. Click *Add*
3. Enter the first name and last name of the user and the desired username.  Click *NEXT*
4. Give the user a strong password and click *Create User*

# Connect to ownCloud using a web browser
In an incognito/private browser window, navigate to the ip address that was set up in step 7 of the *Installation of ownCloud server* section.  You will be presented with several options.

![options](../../../../images/options.png)

Select *ownCloud* under *Applictions*
Enter the username and password that was created in the *Adding a user account* section.
You will then be presented with your documents contained within ownCloud.  

![final screen](../../../../images/finally.png)

Installation completed.  To find out more about using ownCloud, go to our [documentation section](https://doc.owncloud.com/server/index.html)

