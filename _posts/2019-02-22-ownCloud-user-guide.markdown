---
layout: post
title:  "ownCloud Quickstart Guide"
date:   2019-02-22 15:40:15 +0000
categories: 
---

## Introduction
The purpose of this document is to guide users through the installation of the ownCloud server, adding users and accessing the ownCloud server using a client applications.  This document is written specifically for installation on an Apple Mac running OSX High Sierra version 10.13.6 or higher.  Note that this document details an installation for demonstration purposes only.  This method must not be used for a production installation.

## What is ownCloud?
ownCloud is a service that provides cloud storage, file synchronization, personal cloud, and client software applications for individual users and enterprise organisations within an on-premise, secure cloud infrastructure that is within the owners control.  
Architecturally, the software utilises a client-server model, where documents and other software assets are stored on servers and can be accessed through multiple client applications.  ownCloud is an ideal solution for sharing files with select users securely.

## Installed Prerequisites
For the purposes of this installation, the ownCloud server will run on Oracle VM VirtualBox, a free and open-source hosted hypervisor.  A Virtualbox instance will allow a simple and quick installation for demonstration purposes.  Virtualbox for OSX is available from the [Virtualbox site](https://download.virtualbox.org/virtualbox/6.0.4/VirtualBox-6.0.4-128413-OSX.dmg).

## Method
# ownCloud server Installation
1. Obtain an image to run on virtualBox by opening the [ownCloud downloads page](https://owncloud.com/download/) in your browser and downloading the image by clicking the "DOWNLOAD" button in the "Download ownCloud Server" section.  You will be expected to register with ownCloud at this stage in the process.  Enter your details, making sure that you submit a **valid email address** (this will be used to send your license to) and also ensure that the Download version that you select is the _ownCloud Server Appliance (VirtualBox)_ version.

2. When the image has downloaded, launch virtualBox and select *File* - *Import Appliance*.  Click on the folder icon and browser to select your image.  Click *Continue* to proceed to the *Appliance Settings* screen.

3. Leave the settings at their defaults and press *Import*.

4. Press *Agree* to agree to the terms and conditions of the image license agreement and the import will commence.

5. When the import has completed, select the *UCS 4.3-with-ownCloud* image in the left hand column in virtualBox and press *Start*.  The virtualBox image will launch and you will be presented with 3 options.  Allow the boot process to proceed with the *start owncloud* option by default.

6. As this is a first installation, you will be asked several questions for configuration purposes.  Enter your preferred language and city and click *NEXT*

7. In the *Domain and network configuration* section, make sure that *Obtain IP address automatically (DHCP)* box is checked, leave the remaining fields with their default values.  Note the value of the *IPv4/IPv6 address*, as this will be needed later, and click *NEXT*

8. A warning message will appear listing servers that cannot be reached.  Press *Continue without access to the repository servers*

9. For the *domain setup*, leave the *Manage users and permissions directly on the system* option selected and click *NEXT*.

10. In the *Account Information* section, enter your organisation name, a valid email address and a strong password.

11. In the *Host Settings* section, leave the default values and click *NEXT*.

12. Click on *Configure System* and, when the setup has completed, click *FINISH*.

The server has now been installed.  Proceed immediately to the next step

# ownCloud server Setup

**Note that the ownCloud server portal is rendered over http, not https, by default and may be insecure.**

1. Start up a session in your web browser and navigate to the ip address that was set up in step 7 of the *Installation of ownCloud server* section.  This address will also be displayed just after the server has been installed.  i.e.
![server start](../../../../images/server_start.png)
2. You will be asked to activate your license, which will have been sent to you, by email, in a ucs.license file when you originally registered with ownCloud (see step 1 of the *Installation of ownCloud server* section).  Check your inbox for the email and detach the license file in a secure location.

3. Click on *Upload Licence Data* and then click on *FINISH* when the "Activation Successful" message is displayed.  You will now be directed to the welcome screen.  Take note of the administrator username and password that is displayed there.  You may also be asked a couple of survey questions.  Answer them as you see fit and click finish.

# Adding a user account
1. On the main screen, click on the *Users* block.  You will be brought to the *Users* section which will list one user (Administrator).
2. Click *Add*.
3. Enter the first name and last name of the user and the desired username.  Click *NEXT*.
4. Give the user a strong password and click *Create User*.

# Connect to ownCloud, as a client, using a web browser
1. In an incognito/private browser window, navigate to the ip address that was set up in step 7 of the *Installation of ownCloud server* section. 

2. You will be presented with several options.
![options](../../../../images/options.png)

3. Select *ownCloud* under *Applications*.
Enter the username and password that was created in the *Adding a user account* section.
You will then be presented with your documents contained within ownCloud.  
![final screen](../../../../images/finally2.png)

# Connect to ownCloud, as a client, using a desktop app
The OSX ownCloud desktop app is available from the [ownCloud downloads](https://owncloud.org/download/#owncloud-desktop-client-macos) site.  

1. Download the *Testpilot cloud* version and install the app.

2. Upon launching the app, you will be asked for the *Server Address* of the ownCloud server.  Enter the ip address from step 7 of the *Installation of ownCloud server* section.  Click *Next*.

3. When you get a warning about the current SSL connection, click *Trust this certificate anyway* and click *OK*.

4. When prompted for username and password, enter the details of the user created in the *Adding a user account* section.

5. Ensure that *Sync everything from server* is selected and click *Connect*

This completes the installation of the ownCloud OSX client application.

## Installation complete
Now that the installation has completed, you can find out more about using ownCloud by going to the [documentation section](https://doc.owncloud.com/server/index.html).
