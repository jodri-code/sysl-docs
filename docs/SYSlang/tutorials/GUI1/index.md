# [SYSlang Docs - Making A GUI: The Base](https://systemware.ga/SYSlang/#index)

_ngl i didn't wanna write this_

So, you made a login form. Great, now try this: making a Graphical User Interface.

_idek y but these things needs binary files bruh wth..._

Don't worry tho, the [SBF (SYSlang Binary File)](https://github.com/CKStudios2018/SYSlang/blob/main/Core/trans-defs) works on all GUI/Launchers, so just download the loaf and use that. seriously. (I think it may be corrupt on gh atm tho, check the issues tab on that repo to stay updated)

## Part 1: Setting up monitor, to not make pc go boom pls

Simple enough; make an `entry.SYSl` file, and start writing.

This is all the code you need:
```SYSl
require monitor;
//example code hiring here
//sorry, I meant example code here
```
**_yes, comments in SYSlang are double slashes_**

## Part 2: Adding our other essentials.
Next, you will want to import your other essentials, such as the `test_V` lib.

Although test V is mainly a community managed library, it has many essential folders which are locked and cannot be edited by the public.
One of these impressive folders is `GUIs`; the folder that contains all the essentials for making and using GUI/Launchers. We will enter that folder also.
```
require monitor;

lang-imp test_V;

from test_V enter GUIs;
```
*leaving a line between each line of code is **not** necessary, but I like to separate my code.

## Part 3: doodoo, translate time

Next we will need some translators. There aren't a whole lot of these at the minute, but for now we have C (C), JavaScript (JS), C# (C#), C++ (CPP), Ruby (Ruby), Python (Py), Java (Java) and Lua (LUA).
You can add any of these you wish, but you may aswell add all of them, as they are all 1 Mib files (Lua is actually 0.97 Mib), and therefore won't even affect the performance, installation time, or boot time.

Simply add a `for translators(){}` method.
```
require monitor;

lang-imp test_V;

from test_V enter GUIs;

for translators(C, JS, C#, CPP, Ruby, Py, Java, LUA){
    dl(from('systemware.ga/trans/') enter all).to('A:/')
}
```
And now you have a simple script in nogui that can understand any of the languages in the `for translators(){}` method.
Oh, by the way, this thing won't even launch, you will need to finish **all** of these Graphical Launcher tutorials to get it to launch correctly.

### [Return](https://systemware.ga/SYSlang/#index)
### [Take Me To The Next Tutorial](https://systemware.ga/SYSlang/tutorials/GUI2)
