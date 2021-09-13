 
# [Making A GUI - The Base](https://docs.pipewarp.co.uk/SYSlang/#Index)

## _ngl i dont wanna write this_

So, you made a login form. Great, now try this: making a GUI.

_idek y but one of these things needs binary files bruh wth..._

Don't worry tho, the SBF (SYSlang Binary File) works on all GUIs, so just download the loaf and use that. seriously.

## Part 1: Setting up monitor, to not make pc go boom pls

Simple enough; make an `entry.SYSl` file, and start writing.

This is all the code you need:
```
require monitor;
//example code hiring here
//sorry, I meant example code here
```
**_yes, comments in SYSlang are double slashes_**

## Part 2: Adding our other essentials.
Next, you will want to import your other essentials, such as the `test_V` lib.

Although test V is mainly a community managed library, it has many essential folders which are locked and cannot be edited.
One of these impressive folders is `GUIs`; the folder that contains all the essentials for making and using GUIs. We will enter that folder also.
```
require monitor;

lang-imp test_V;

from test_V enter GUIs;
```
*leaving a line between each line of code is **not** necessary, but I like to separate my code.

## Part 3: Beating the ex-es.
Now that we have entered the GUIs folder, we can use `ex`.

`ex` is a GUI-only command, that disables other elements that can interfere or cause interferences with our GUI.

There is a long list of apps and services that can interfere or cause an interference with your GUI when running a VM on SYStemware, so look into that [here](https://docs.google.com/document/d/1pGIEeBDoBy7iL85BabAjHRIA6SznABof1AjNUcOL6xE/edit?usp=drivesdk)

To disable any of these, use `ex.disable.'app here'` or `ex.disable.d.'app service initial'.'app name'` (some app services have two service initials)

## Part 4: Google Translate
_(I will change this name when I find a funnier joke)_

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
And now you have a simple GUI in nogui that can understand any of the languages in the `for translators(){}` method.
Oh, by the way, this thing won't even launch, you will need to finish **all** of these GUI tutorials to get it to launch correctly.

## [Return](https://docs.pipewarp.co.uk/SYSlang/#index)
## [Take Me 2 The Next Tutorial M8](https://docs.pipewarp.co.uk/SYSlang/tutorials/GUI2)
