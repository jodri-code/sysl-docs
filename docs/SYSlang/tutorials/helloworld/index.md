# Hello World in SYSlang


### huh, y so long?

## This section is _once again_ for the very new users of SYSl

Welcome to the first tutorial on this site.

In this tutorial you'll learn:
* How to use the `nogui` class to 'write' text in a CLI.
* How other 'write' functions work.
* How to make a small, yet functional text-based welcoming system for entering a new username.

## Before you start:
This tutorial is designed for _new_ users using SYStemware's Coderttop, or SYSlang's CLI on Windows/Linux.

## Part 1: Making the new save file
To make a new file (and to overwrite it in the near future) type `savefile` and type the name afterwards.
By default Script's will be saved in the same folder as the CLI is in.

To save the open file as a new file, use `savefile.new()` and type the new name in the brackets.

## Part 2: Writing the new file out
Once you have successfully saved the file, to start typing code inside use `editscript()` and type the file name in the brackets.

While here on CMD or Terminal in Windows or Linux, there will be **no** auto corrector or code checker.

Start typing your code, here is a nice example to get a basic hello world written on the screen:
```
if(time('x').wait('printout()'));

printout('txt'){
  'Hello'+cha37&+'world'
}.print(to('nogui'));
```

Lets go over what happens here:

`if(time('x'))` means that if the time is superior to x then continue. The only alternative is to make the file execute when opened, or to constantly execute on a loop.
The reason the time has to be superior to x is because its a 24h time set in ms, so 0 equals 12:00pm (00:00)

`time().wait('printout()'` waits for printout to execute if the time is superior, in our case, to x. To make it inferior you could do -x, but that's useless because it will still always work.

`printout('txt')` declares our method printout. You can call it anything, but to get the space between hello and world, you need to declare its text in brackets.

`cha37&` is the key code for a space. If you were to put spaces in the comas, SYSlang would return null, as it only supports one word in the commas, without spaces.
There is a code mod coming out that should by auto-replacing the invalid characters for valid ones.

`.print(to('nogui'))` prints your text in the nogui.

[My head's hurtin', less read s'more](https://docs.pipewarp.co.uk/SYSlang)
