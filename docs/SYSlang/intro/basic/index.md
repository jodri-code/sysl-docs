## [SYSlang Basics](https://docs.pipewarp.co.uk/SYSlang/)

# Part 1: Setting up the CLI
### haha powershell go brrr

## Skip this part if you are _not_ using Windows!
[Download link for Windows (x32)](http://systemware.ga/cli-windows32-latest/)

This _part_ is for the users that are on Windows and have PowerShell (usually Windows 10).

Don't worry if you _don't_ have Windows or PowerShell, further along in this guide there's a section for you!

# Downloading & Installing the CLI (Windows/PowerShell)
The installation process is simple enough, download the file, and open it. Once the installer opens, agree to the T&C's and it will install itself.

This is where it gets a bit more complicated. Because of Windows 10 wanting to use PowerShell and it's respective ISE from factory, you will have to manually go to settings and change the default from PowerShell to CMD.

Usually, this is done by going to settings, personalization and taskbar settings. From here there is a setting that says something like 'Replace Command Prompt with PowerShell'. If that setting is enabled, you will have to disable it.

If however, you are using Windows 8 or below and this setting does not apply, feel free to remember you just wasted 5 minutes reading all of that.

## Skip this part if you are _not_ using Linux
[Download link Linux](http://systemware.ga/cli-linx-latest/)

This _part_ is for Linux users.

# Downloading and Installing the CLI (Linux/Terminal)
There are two ways of downloading the CLI attributes for Linux: Via Download Link or as a lib via the Terminal. I _won't_ be explaining the latter.

Once the file is downloaded, right-click the downloaded file and go to 'properties'. Once there, you need to allow execution as an app.

Then you can simply open the downloaded file, and it should open a Terminal window and print `Wares CLI`.

## Skip this part if you are _not_ using SYStemware
This _part_ is for SYStemware users.

# Downloading and Installing the CLI (SYStemware Codertop/Testtop)
There are two ways of using the CLI in SYStemware. One is selecting Codertop upon initiation. SYStemware will do the rest, no install required.

The other method is using the more day-to-day friendly Testtop. To install the CLI here, you can simply go to settings and select 'Consoles'. Here you tick 'Ware's CLI' and SYStemware will begin the download. The installation process is also automated, but after SYStemware v51.x a restart is required.

If that didn't work out for you, you can simply manually [Downlaod for Ware](http://systemware.ga/cli-4kill64x86-latest/)

# Part 2: Using the CLI
### no, i'm not explaining how to double click an app

## This part is dedicated for _new_ SYSlang users. It will go over the _very basics_ of the CLI.
Some requirements to understand before attempting anything:
- If you want to code something with a GUI (Graphical User Interface), you will need to add [Monitor](https://docs.pipewarp.co.uk/SYSlang/class/monitor)
- As a precaution, if you want to make _anything that is similarly GUI based_ (game, client, OS, ect.) you should add some [resourceLevel controls](https://docs.pipewarp.co.uk/SYSlang/cautions/)

# Using the CLI on Windows
Open CMD as an Administartor. The easiest way to do this is to use Windows key + x (at the same time) and choose 'Command Prompt (Admin)'.

Once CMD has opened, type 'cd your default drive:\your user name\Documents\SYSl' replacing "your default drive" with your default drive's letter (such as C, ect) and "your user name" with your user name (the one you are currently logged in as would help).

Once you've sorted that, type "start.SYSl" to start SYSlang's CLI on Windows.

If you did that right, "Wares CLI" should show up as your user/drive letter on the command line
# Using the CLI on Linux
Well, the file is probably on your home screen, but if not you can try:

Open terminal. Type "start.SYSl". It opens in a new terminal window.

_Note: you can't close the first Terminal Window_

# Using the CLI on SYStemware
Protip: use SYStemware's Codertop for an optimised experience.

On SYStemware's Testtop, open CLI in the Shortcuts menu after installing.

## [Return to Start](https://docs.pipewarp.co.uk/SYSlang/#Index)
