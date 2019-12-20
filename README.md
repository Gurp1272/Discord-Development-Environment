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

**Run**

```
sudo apt-get update
```

```
sudo apt-get upgrade
```

```
sudo apt-get install dkms
```

```
reboot
```

Click ***Devices*** at the top of the window then click ***Choose a disk file...***

Navigate to ***C:/Program Files/Oracle/VirtualBox*** and select ***VBoxGuestAdditions***

Open a terminal window and navigate to ***/media/user/VBox_GAs_6.1.0***

**Run**

```
sudo ./VBoxLinuxAdditions.run
```

```
reboot
```

Remove Guest Additions from the virtual optical drive

## Install Ruby and pull in discordrb dependency

Open terminal

**Run**

```
sudo apt-get install ruby-full
```

```
sudo gem install discordrb
```

## Optional Install of Emacs26 as text editor

Open terminal

**Run**

```
sudo add-apt-repository ppa:kelleyk/emacs
```

```
sudo apt-get update
```

```
sudo apt install emacs26
```

Once that is installed. To create a file to edit ***Run***

```
sudo emacs -nw example.rb
```
This opens the file in bash editor

To open emacs in window mode, leave out the ***-nw***

## Useful documentation and resources

>https://discordapp.com/developers/docs/intro

>https://github.com/discordrb/discordrb/wiki/Basic-bot-creation

>https://github.com/discordrb/discordrb/wiki/Events

>https://www.rubydoc.info/gems/discordrb/Discordrb

>https://github.com/AnIdiotsGuide/discordjs-bot-guide/blob/master/understanding/events-and-handlers.md




