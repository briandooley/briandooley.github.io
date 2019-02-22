---
layout: post
title:  "ownCloud Quickstart Guide"
date:   2019-02-20 15:40:15 +0000
categories: 
---

## Introduction
The purpose of this document is to guide users through the installation of ownCloud server, adding users and accessing the ownCloud server via a client application in a short timeframe.  This document is written specifically for installation on an Apple Mac running OSX High Sierra version 10.13.6 or higher.  Note that this document details an installation for demonstration purposes only.  This method must not be used for a production installation.

## What is ownCloud?
ownCloud allows individual users and enterprise organisations to host their documents within a on-premise, secure cloud infrastructure that is entirely within the owners control.  In terms of architecture, the software utilises a client-server modal, where documents and other software assets are stored on servers and can be accessed through multiple client applications. 

## Installed Prerequisites
This guide covers the installation the ownCloud server on a virtualbox instance since this allows a simple and quick installation for demonstration purposes.  Virtualbox version 5.2.26 for OSX is available [here](https://download.virtualbox.org/virtualbox/6.0.4/VirtualBox-6.0.4-128413-OSX.dmg) 

## Method
# Installation of ownCloud server
1. Obtain an image to run on virtualBox.  Open [https://owncloud.com/download/](https://owncloud.com/download/) in your browser and download the image via the "DOWNLOAD" button in the "Download ownCloud Server" section.

You will be expected to register with ownCloud at this stage in the process.  Enter your details, making sure that you submit a _valid email address_ (this will be used to send your license to) and also ensure that the Download version that you select is the _ownCloud Server Appliance (VirtualBox)_ version.

![Download details](../../../../images/downloaddetails.png)

2. When the image has downloaded, launch virtualBox and select **File** - **Import Appliance**.  Click on the folder icon and browser to select your image.

Click **Continue** to proceed to the **Appliance Settings** screen.

3. Leave the settings at their defaults and press **Import**.

4. Press **Agree** to agree to the terms and conditions of the image license agreement and the import will commence.

5. When the import has completed, select the *UCS 4.3-with-ownCloud* image in the left hand column in virtualBox and press *Start*.  The server will present 3 options.  Allow the boot process to proceed with the *start owncloud* option by default.

6. As this is a first installation, you will be asked several questions for configuration purposes.  Enter your preferred to language and city and click *NEXT*

7. In the *Domain and network configuration* section, make sure that *Obtain IP address automatically (DHCP)* box is checked, leave the remaning field with their default values and click *NEXT*

8. A warning message will appear listing servers that cannot be reached.  These will be configured later so, for the moment, press *Continue without access to the repository servers*

9. For the *domain setup*, leave the *Manage users and permissions directly on the system* option selected and click *NEXT*.

10. In the *Account Information* section, enter your organisation name, a valid email address and a strong password.

11. In the *Host Settings* section, leave the default values and click *NEXT*.

12.  You are all set.  Click on *Configure System* and, when the setup has completed, click *FINISH*.

The server is now configured.












![Image of Yak](../../../../images/2001-1.jpg)


You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/