## [SYSlang Docs Index](https://docs.pipewarp.co.uk/SYSlang/)

# This section is dedicated to some precautions for SYSlang
### don't make pc go boom pls

# Monitor class precautions
The first type of precautions are for the most consuming part of SYSlang, it's GUI. Some precautions can save entire PC's, so use them wisely!

As safety comes first, we highly recommend setting a resourceLevel. This specific precaution is largely forgotten by even the devs that made the lang, but can save _hundreds_ of dolars and _thousands_ of lives. Monitor provides this feature by default, but it's not set to anything until it's called. To call it, just type `monitor.setResourceLevel(auto)`. This case will automate the use of resources and will adjust the ventilators, clock timings and, depending on your PC build, even adjust the frequency that your CPU or RAM run at.

This can be extremely useful for saving PC's, especially if you don't know how much weight your app will have on devices. 

# OS Build Precautions
Another good precaution is to watch over the OS build. This was irrelevant until InfDev found that there is a way to expose the entire core code by allowing the OS to build incorrectly.

The OS build is always a value of 0, 0.5 or 1. 0 is a complete fail, 0.5 is a faulty install and 1 is a correct install. This can be checked after the ag (after girth) has run using the diagnostics window and going to the 'Build' tab.

This mainly happens when the disk isn't formatted correctly or isn't partitioned in at least 3 parts.

To make sure you have a correctly formatted disk you can do `format.this(ch)` or to check the partitions you can do `part(ch)`.
You can run these commands during installation or once booted, but I recommend running them during installation. 
