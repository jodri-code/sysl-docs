## [SYSlang Docs - Precautions](https://docs.pipewarp.co.uk/SYSlang/)

# This section is dedicated to some precautions for SYSlang
### don't make pc go boom pls

# Monitor class precautions
The first type of precautions are for the most consuming part of SYSlang, it's GUI. Some precautions can save entire PC's, so use them wisely!

As safety comes first, we highly recommend setting a resourceLevel. This specific precaution is largely forgotten by even the devs that made the lang, but can save _thousands_ of dolars and _hundreds_ of lives. Monitor provides this feature by default, but it's not set to anything until it's called. To call it, just type `monitor.setResourceLevel(auto)`. This case will automate the use of resources and will adjust the ventilators, clock timings and, depending on your PC build, even adjust the frequency that your CPU or RAM run at.

This can be extremely useful for saving PC's, especially if you don't know how much weight your app will have on devices. 

# OS Build Precautions
Another good precaution is to watch over the OS build. This was irrelevant until InfDev found that there is a way to expose the entire core code by allowing the OS to build incorrectly.

The OS build is always a value of 0, 0.5 or 1. 0 is a complete fail, 0.5 is a faulty install and 1 is a correct install. This can be checked after the ag (after girth) has run using the diagnostics window and going to the 'Build' tab.

This mainly happens when the disk isn't formatted correctly or isn't partitioned in at least 3 parts.

To make sure you have a correctly formatted disk you can do `format.this(ch)` or to check the partitions you can do `part(ch)`.
You can run these commands during installation or once booted, but I recommend running them during installation.

# Hotspot and VPN's
The hotspot is a useful feature. Unfortunately, the password used to get leaked. That is now fixed.

VPN usage on SYStamware is extremely difficult and dangerous for those who don't know what they're doing.

If **YOU** don't know how to use a VPN on SYStemware, _don't_. There is absolutely no need.

# IP's
SYStemware will provide you with a private IP known as a SIP (Secure Internet Protocol) with a randomised IP not dependant on the DNS configurations of your modem/router, which remains completely anonymous to your ISP.

These SIP's show gov.cks as your location (mock IP, mock location). This is possible thanks to SYStemware's IP cloacking, and the gov.cks programme, that has short over 256 million different possible SIP's.

The SIP is also randomised on boot, so you and/or anyone else will have a different SIP when your device restarts. You may, overtime, get a previously used SIP. There is absolutely nothing to worry about, all traces stay where they were made.

## [Return to Start](https://docs.pipewarp.co.uk/SYSlang/#index)
