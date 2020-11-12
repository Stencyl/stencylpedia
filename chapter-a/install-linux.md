> **Call for Help:** Want to help us improve this article? [Propose edits](https://github.com/Stencyl/stencylpedia/edit/master/chapter-a/install-linux.md) to this article.
<br/><br/>
> **Note:** This article pertains only to Linux. On Mac and Windows, nothing extra needs to be done on your part to install Stencyl (besides running the Windows installer or dragging the app folder to the Mac's Applications directory).
## Installation instructions for Ubuntu 20.04 and Mint 20

Download and extract Jar file. 
Insure system is updated.
Run the Stencyl file which can be found 
"Download Location"/Stencyl-4.0.4-linux$ ls
behaviors  data  ext-tools  lang  plaf  prefs  runtimes  Stencyl  sw.jar

To make a launcher in Ubuntu follow the instructions shown here. 
https://askubuntu.com/questions/1184733/gnome-desktop-item-edit-command-not-found-on-ubuntu-19-10-and-later-even-with-t

With the application path as given above. 
And icon path here
"Download Location"Stencyl-4.0.4-linux/data/other/icon-30x30.png

## Installation instructions for Ubuntu and Debian -- Older Verisons 

> *Note:* Installation on other Linux distributions will be similar, but the package names may be different. If you have trouble installing Stencyl on another Linux distribution, [ask on the forums](http://community.stencyl.com/index.php/topic,30927.0.html).

#### Minimum Requirements
* Ubuntu 12.04 LTS or later OR Debian Jessie or later.
* libc6 2.15 or later. *(Haxe 3.0+ does not work with older versions of libc6)*

<br/>

#### Step 1 - Install the Compiler and its Dependencies
Run the following command:

```
sudo apt-get install g++ libgc-dev libxext-dev
```
 
> *Perform steps 2 and 3 only if you are on a 64-bit Linux system. If you are on a 32-bit system, you may now run Stencyl.*

 
#### Step 2 - Install Packages required by the JRE and Android SDK
If you are on **Debian**, first add the 32-bit architecture to the package manager:

```
sudo dpkg --add-architecture i386
sudo apt-get update
```

Run the following command to install the packages needed by the JRE and the Android SDK:

```
sudo apt-get install libstdc++6:i386 libxtst6:i386 libxext6:i386 libxi6:i386 libncurses5:i386 libxt6:i386 libxpm4:i386 libxmu6:i386 libxp6:i386
```
 

#### Step 3 - Install Packages required by Flash Player
Run the following command to install the packages needed by the standalone Adobe Flash Player:

```
sudo apt-get install libgtk2.0-0:i386 libxt6:i386 libxext6:i386 libatk1.0-0:i386 libc6:i386 libcairo2:i386 libexpat1:i386 libfontconfig1:i386 libfreetype6:i386 libglib2.0-0:i386 libice6:i386 libpango1.0-0:i386 libpng12-0:i386 libsm6:i386 libx11-6:i386 libxau6:i386 libxcursor1:i386 libxdmcp6:i386 libxfixes3:i386 libxi6:i386 libxinerama1:i386 libxrandr2:i386 libxrender1:i386 zlib1g:i386 libnss3-1d:i386 libnspr4-0d:i386 libcurl3:i386 libasound2:i386
```

 
#### Step 4 - Install JDK 8 to be able to test or export to Android
Run the following command to install JDK 8 from [WebUpd8 PPA](https://launchpad.net/~webupd8team/+archive/ubuntu/java):

```
sudo apt-add-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

When asked by Stencyl for the location of Java, navigate and select 
```
/usr/lib/jvm/java-8-oracle 
```


## Installation Instructions for Arch Linux

[View this page](http://community.stencyl.com/index.php/topic,32022.0.html)
