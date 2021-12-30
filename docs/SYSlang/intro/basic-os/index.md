# [SYSlang Docs | Install Guide](https://docs.pipewarp.co.uk/SYSlang)


### uhh... new Operating System!! Link now available!!!

Ok, so its been a while since i did some good docs, here we go...

SYStemware: that one OS designed to try everything.

Its so difficult to install that I'm rewriting the installer. People are gonna hate me for the delay... but heres the (semi-updated) guide:

# Downloading the OS
Obviously I'd recommend you download over wifi only, its about 5 Gb

[download link wooo!](http://systemware.ga/download-latest/)
[download mirror (Google Drive)](https://drive.google.com/file/d/1hsgSxpMeA2Gwo6gfydwm60BYbVmTOnCr/view?usp=sharing)

# Installing the OS
### Using a Virtual Machine is recommended for new users

So, there's two (main) ways to go about the install:

* Live Install: the OS is on a flash and you plug&play
or
* Full Install: the OS encrypts your PC's drive

## Full install:

I'll go over it for virtual machines for now (although the Live Install only really differs where you save the OS `boot()`):

Insert the ISO file into the CD drive of the virtual machine and wait for the os to boot into the installer.

# If prompted for type of Install (Versions above v62.04-rc1)
Simply select SeaBIOS Install. The other options require a Dev Key; a 48-digit key that unlocks the bootloader.

Once the installer has begun, there's two ways to install the OS, guided (with GUI) or nogui install (Default)

The guided GUI install can be activated once you have partitioned the disk and rebooted.

## Disk formatting and partitioning

It's recommended to have at least 12Gb for the installation plus 6Gb for installation files. The minimum you can install on is 18.7Gb

To partition the disk, you will first have to format the disk (format.this().size('your available space here/"all" to erase and format the entire disk')

Once formatting has completed, nogui should prompt ">1: ". This is prompting you to name the first partition (I recommend boot, primary, secondary). Hit enter after naming it to name the next partition.

You will have to repeat this process until you press `ctrl+c`, and it will continue to make partitions (sometimes even fake ones) until you do.

To get the best performance, I recommend you have only 3 partitions and name them:

* 1: boot
* 2: primary
* 3: secondary

Once you have named these partitions, press the `ctrl+c` combination after pressing enter for the 3rd time, to reboot the OS.

## Opening the Guided Installer
Once rebooted, to open the guided installer simply type `inst(gui)` and press enter.

The installer will make things harder for those who are new tho.

## Installing without the guided installer
To install without said guided installer, type `part(ch)` to see if you have the 3 partitions. (This step is unnecessary but i always do it to be sure)

To proceed 'coubana' is the install code. Plz dont ask.

The installer will prompt with "are you sure y/n:", just type `y` and hit enter. If you're using version 63.01 or earlier type `g` instead to see a cool bug.

The nogui should now ask you to enter your SSID. Dont worry about this, its an internet thing. On VirtualBox, typing anything works, as long as you leave the password as "none."
If you are not however on a virtual machine, you should enter a real SSID from a real network that you also have the password to.

After entering the SSID, "pass:" should show up. Enter the wifi password. To skip don't type anything and hit enter. If its incorrect, it will prompt for the password again.

The installer should proceed to download & install everything from the file server.

## Opening the OS in nogui

To complete the installation, username and password creation _won't_ popup anymore. Your username will be user1 and there will be no password until you set it in settings.

So, how do you get in? Well...

First you need to type `ag().ch`

This confirms the installation (both with the server and on the machine itself)
This also assigns you your private IP.

The meaning of `ag()` tho, is after girth, a meme-ish name Chawi gave the afterinstaller.

And in case you didn't get it by now, `.ch` and `(ch)` is check, as in, verify.

Once the check is complete your screen should go black and all the writing should disappear and then basically look like a fresh nogui was opened.

Type `gui(ch)` and you should see 3 GUI's downloaded. This is because SYStemware comes with three different modes:
* Desktop - A normal multi-functional Desktop
* Gamertop - A Desktop optimised for games
* Codertop - A Desktop optimised for code development

You can download more user created GUI's from GitHub.com, or the built-in repos (a lot harder, no I'm not explaining)

## Actually getting in to the OS, at last.
These commands are unique to everyone's build, but to get to the default GUI's:

Reboot. This will open Testtop.

If you hold c while booting, nogui will load instead.
From nogui:

* Desktop():
Loads Testtop (bruh it default lmao)
* Game():
Loads Gamertop (pipewarp hasn't published the main engine, currently has a template game (dev) engine)
* Code():
Loads Codertop (Advanced Code Tips!)

# [Return to start, my head hurts](https://docs.pipewarp.co.uk/SYSlang)
