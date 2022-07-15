# [SYStemware Docs | Install Guide](https://jodri-code.github.io/sysl-docs/)


### uhh... new Operating System!! Link now available!!!

SYStemware: that one OS designed to try everything.

Its so difficult to install that I'm rewriting the installer. People are gonna hate me for the delay... but heres the (semi-updated) guide:

# Downloading the OS
Obviously I'd recommend you download over wifi only, it's about 1 Gb

[download link](http://systemware.ga/download-latest/) | [download mirror (Google Drive)](https://drive.google.com/drive/folders/1cTcVfbwneRS8MPR9nBEi1dHLd1_q-_G_?usp=sharing)

*The Google Drive Mirror is a folder containing multiple ISO's; SYStemware.iso is always the last updated version (all other versions get deleted after a while, renamed once an update is pushed)

# Installing the OS
### Using a Virtual Machine is recommended for new users
So, there's two (main) ways to go about the install:

* Live Install: the OS is on a Flash (USB) and you plug&play
or
* Full Install: the OS encrypts your PC's drive

**It's recommended to have at least 8Gb for the installation plus 6Gb for installation files. The minimum you can install on is 12Gb

## Full install:
I'll go over it for virtual machines for now (although the Live Install only really differs where you save the OS `boot()`):

Insert the ISO file into the CD drive of the virtual machine and wait for the OS to boot into a nogui window.

There are two ways to install the OS, guided (with GUI) or nogui install (Default)

The guided install can (currently) only be activated once you have partitioned the disk and rebooted. I'm changing this.

## Run the Installer
So, the first thing to get running is the installer.

The command to execute the installer used to change, but now we are sticking with `roxio`

A few binaries will run on slower devices, but once the screen clears, continue.

## Disk formatting and partitioning
To partition the disk, you will first have to format the disk `(format.this().size(`'your available space here/"`all`" to erase and format the entire disk'`)`

Once formatting has completed, nogui should prompt ">1: ". This is prompting you to name the first partition. Hit enter after naming it to name the next partition.

You will have to repeat this process until you press `ctrl+c`, and it will continue to make partitions (eventually even fake ones) until you do.

To get the best performance, I recommend you have only 3 partitions and name them:

* 1: `boot` (you can put this one anywhere, but it's recommended to put it first as it can then take up all the space it needs)
* 2: `primary` (master slave; users, program data and binaries are stored here; add before secondary for better performance)
* 3: `secondary` (any other space will get taken up by a partition named secondary, so anything after this will be a fake partition)

Once you have named these partitions, press the `ctrl+c` combination after pressing enter for the 3rd time, to reboot the OS.

## Opening the Guided Installer
Once rebooted, to open the guided installer instance simply type `inst(gui)` and press enter.

The guided installer is undergoing some rewrites to make things easier. Also it bugs out loads.

## Installing without the guided installer
Type `setup` to continue without a GUI Install.

The nogui should now prompt you to enter your SSID. Dont worry about this, its an internet thing. On VirtualBox, typing anything works, as long as you leave the password as "none".

If you are not, however, on a virtual machine, you should enter a _real_ SSID from a _real_ network that you also _own_ the password to.

After entering the SSID, "pass:" should show up. Enter the wifi password. To skip don't type anything and hit enter. If its incorrect, it will prompt for the password again after a few seconds.

The installer should proceed to download & install everything from the file server.

## Opening the OS in nogui
To complete the installation, username and password creation _won't_ popup anymore. Your username will be user1 and there will be no password until you set it in settings.

So, how do you get in? Well...

First you need to type `ag().ch`

This confirms the installation (both with the server and on the machine itself)
This also assigns you your private IP.

Once the check is complete your screen should clear and reboot. If this is not the case, contact us at [ckstudios2003@gmail.com](mailto:ckstudios2003@gmail.com) and send us the error code or debug log that appeared on your screen.

## EJECT THE MEDIUM!
This may sound silly, but VirtualBox doesn't eject the disk for you. You should do that, even if you are installing from a USB on a physical machine, eject the medium.

If you fail to do this, the installer will restart. But don't worry if it restarts before you can do this. Simply eject it before trying to install again and use `ctrl+c` to reboot.


You can type `gui(ch)` and you should see 3 GUI's downloaded. This is because SYStemware comes with three different modes, that are automatically installed in versions above 62;
* Testtop - A normal multi-functional Desktop
* Gamertop - A Desktop optimised for games
* Codertop - A Desktop optimised for code development

You can download more user created GUI's from GitHub.com, or from the testV shared drive (a lot harder, not explained here)

## Actually getting in to the OS, at last.
If you hold `c` while booting, nogui will load.
From nogui:

* `Desktop()`:
Loads Testtop (it's also the default if you don't press `c`)
* `Game()`:
Loads Gamertop (pipewarp hasn't published the main engine, currently has a template game (dev) engine). Not many playable games translated.
* `Code()`:
Loads Codertop (Advanced Code Tips!). Only supports translated languages (see the gdoc for more info).

These commands are the default, but can vary on anyone's build.

# [Return to start, my head hurts](https://jodri-code.github.io/sysl-docs/)
