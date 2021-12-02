# [SYStemware Documentation](https://docs.pipewarp.co.uk/SYSlang)


### uhh... new operating system link when!!!

Ok, so its been a while since i did some good docs, here we go...

SYStemware: that one OS designed to try everything.

Its sooo difficult to install people are gonna hate me for it... but heres the guide:

# Downloading the OS
Obviously I'd recommend you download over wifi only, its about 6 Gb

[download link wooo!](http://systemware.ga/download-latest/)

# Installing the OS
### virtual machine is recommended for new users

So, there's two (main) ways to go about the install:

* Live install: the OS is on a flash and you plug&play
or
* Full install: the OS encrypts your PC's drive

## Full install:

I'll go over it for virtual machines for now:

Insert the ISO file into the cd drive of the virtual machine and wait for the os to boot into the installer.

Once the installer has begun, there's two ways to install the OS, guided (with gui) or nogui install (default)

The guided GUI install can be activated once you have partitioned the disk and rebooted.

## Disk formatting and partitioning

It's  recommended to have at least 21Gb for the installation plus 6Gb for installation files. The minimum you can install on is 20.2Gb

To partition the disk, you will first have to format the disk (format.this().size('your available space here/"all" to erase and format the entire disk')

Once formatting has completed, ">1: " should show in the nogui. This is prompting you to name the first partition.

You will have to repeat this process until you press ctrl+c, and it will continue to make partitions (sometimes even fake ones) until you do.

To get the best performance, I recommend you have only 3 partitions and name them:

* 1: boot
* 2: primary
* 3: secondary

Once you have named these partitions, press the ctrl+c combination after pressing enter for the 3rd time, to reboot the OS.

## Opening the Guided Installer
Once rebooted, to open the guided installer simply type inst() and press enter.

The installer will make things harder for those who are new tho.

## Installing without the guided installer
To install without said guided installer, type part(ch) to see if you have the 3 partitions. (This step is unnecessary but i always do it to be sure)

To proceed 'coubana' is the install code. Plz dont ask.

The installer will prompt with "are you sure y/n:", just type y and hit enter. If you wanna see a cool bug type g and hit enter.

The nogui should now ask you to enter your SSID. Dont worry about this, its an internet thing. On VirtualBox, typing anything works, as long as you leave the password as "none."
If you are not however on a virtual machine, you should enter a real SSID from a real network that you also have the password to.

After entering the SSID, "pass:" should show up. Enter the wifi password. To skip don't type anything and hit enter. If its incorrect, it will prompt for the password again.

The installer should proceed to download & install everything from the file server.

## Opening the OS in nogui

To complete the installation, username and password creation _won't_ popup anymore. Your username will be user1 and there will be no password until you set it in settings.

So, how do you get in? Well...

First you need to type ag().ch

This confirms the installation (both with the server and on the machine itself)
This also assigns you your private IP.

The meaning of ag() tho, is after girth, a meme-ish name Chawi gave the afterinstaller.

And in case you didn't get it by now, .ch and (ch) is equal to check, as in, verify.

Once the check is complete your screen should go black and all the writing should disappear and then basically look like a fresh nogui was openend.

Type "gui(ch)" and you should see 0 GUI's downloaded. That's because they are on Github.com, and anyone can choose to make their own.

To download the default ones, type "dl(gui().from('https://github.com/CKStudios2018/SYSlang'))". The nogui installer will install the three default GUI's from CKStudios2018 GitHub Account

## Actually getting in to the OS, at last.
These commands are unique to everyone's build, but to get to the default GUI's:

Reboot. This will open Testtop.

If you hold c while booting, nogui will load instead.
From nogui:

* Desktop():
Loads Testtop (bruh it default lmao)
* Game():
Loads Gamertop (pipewarp hasn't published the engine)
* Code():
Loads Codertop (2 nogui's)

# [Return to start my head hurts](https://docs.pipewarp.co.uk/SYSlang)
