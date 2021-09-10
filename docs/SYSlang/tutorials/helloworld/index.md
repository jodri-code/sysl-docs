# Hello World in SYSlang


### huh, y so long?

## This section is for the new(ish) users of SYSl

Welcome to the first tutorial on this site.

In this tutorial you'll learn:
* How to use the `nogui` to 'write' or 'print' text in a CLI.
* How other 'write' or 'print' functions work.
* Some code optimization tips

## Before you start:
This tutorial is designed for _new_ yet somewhat experienced users using SYStemware's Coderttop, or SYSlang's CLI on Windows/Linux.

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

`time().wait('printout()'` waits for printout to execute if the time is superior, in our case, to x. To make it inferior you could do -x, but it will still work only once.

`printout('txt')` declares our method printout. You can call it anything, but to get the space between hello and world, and for SYSlang to understand that this is text, you need to declare it is text (txt) in the brackets.

`cha37&` is the key code for a space. If you were to put spaces in the comas, SYSlang would return null, as it only supports one word in the commas, without spaces.
There is a code mod coming out that should help by auto-replacing the invalid characters for valid ones.

`.print(to('nogui'))` prints your text in the nogui. To see a fun bug caused by the lang changing over time, change this to `.write('printout()')`

## Part 3: `else` and `else if` statements

In SYSlang, there is no else if statement, however you can put if inside if forever, making the code more  complicated, but allowing for more variations of the same.

The final else can be just an else:

```
if(time('x').wait('printout()'));
else(time('-x').wait('return(if)');

printout('txt'){
  'Hello'+cha37&+'world'
}.print(to('nogui'));
```

## [My head's hurtin', less read s'more](https://docs.pipewarp.co.uk/SYSlang/#index)
