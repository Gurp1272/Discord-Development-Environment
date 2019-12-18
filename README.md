# Discord-Development-Environment
Discord Development Environment in Lubuntu using VirtualBox and Ruby

Download VirtualBox for your OS. 

>https://www.virtualbox.org/wiki/Downloads

Download Lubuntu 18.04 Bionic Beaver 64bit
>http://cdimage.ubuntu.com/lubuntu/releases/18.04/release/lubuntu-18.04-desktop-amd64.iso

## VirtualBox initialization
Open VirtualBox and click ***New*** in the top menu

Give your virtual machine a name. 

  Select Type: ***Linux***

  Version: ***Debian (64-bit)***

Leave all settings set to default except:

* Set memory allocation to: ***4028MB***

* Set hard disk size to: ***32GB***

Insert your Lubuntu ISO into the VirtualBox drive, then click __Start__

Proceed through the Lubuntu Setup. Leave all settings default, except:
* What apps would you like to install to start with: ***Minimal Installation***

## Install VirtualBox Guest Additions
When your install is done, you will notice that even when you go fullscreen, the actual viewport stays small. 

Guest Additions fixes this problem

Open terminal

Run

```
sudo apt-get update
```

```
sudo apt-get upgrade
```

```
sudo apt-get install dkms
```

Click ***Devices*** at the top of the window then click ***Choose a disk file...***

Navigate to ***C:/Program Files/Oracle/VirtualBox*** and select ***VBoxGuestAdditions***

Open a terminal window and navigate to ***/media/user/VBox_GAs_6.1.0***

Run

```
sudo ./VBoxLinuxAdditions.run
```

```
reboot
```

Remove Guest Additions from the virtual optical drive

Proceed to ***Preferences*** then ***Monitor Settings***

Change Resolution: ***Auto***





