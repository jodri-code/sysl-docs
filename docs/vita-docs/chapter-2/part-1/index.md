## [PSVita Guide Index](https://docs.pipewarp.co.uk/vita-docs)

# Chapter 2:
# Part 1:
### right, how does the hello world work tho

### A REMINDER!
You don't have to use Ubuntu's default editor, nano if you are having trouble with it. You could try using something like **Vim** or other alternatives

# Part 1: Writing code!
Let's make a basic hello world program. Go into main.c/cpp of the example and erase everything so we can have a fresh start.

# Includes
The first few lines we want to add are some includes!
```cpp
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

#include <psp2/ctrl.h>
#include <psp2/kernel/processmgr.h>

#include <vita2d.h>
```
This includes some necessary PSVita functions, some general C/C++ functions aswell as libVita2D (our renderer).

# Initialisation
Now we add main() (duh) and inside of it, we will add ```cpp vita2d_pgf *pgf;```. This will allow us to put the vita's default font in this variable we can reference later.


Next we add the following, they should be pretty self explanatory.
```cpp
vita2d_init();
vita2d_set_clear_color(RGBA8(0x40, 0x40, 0x40, 0xFF));
```
After that we load the vita's font so we can display text!
```cpp
pgf = vita2d_load_default_pgf();
```
# Loop
Now that thats done, we can move onto the loop.
Add a infinte while loop (```cpp while(1)```) and put the following inside.
```cpp
vita2d_start_drawing();
vita2d_clear_screen();

// our hello world code which we will put in later

vita2d_end_drawing();
vita2d_swap_buffers();
```
This will let LibVita2D when to draw things onto the screen.

# Hello World code
Now, inbetween the start drawing and end drawing lines is where all our code will lie (hence the comment I left in the example above). Delete that comment and replace it with the following:
```cpp
vita2d_pgf_draw_text(pgf, 10, 10, RGBA8(0,255,0,255), 1.0f, "Hello World!");
```
This prints out "Hello World!" onto the screen.
Heres an explanation of the paramaters:
```cpp
vita2d_pgf_draw_text(pgf, // Font 
					 10,                 // X position
					 10,                 // Y position
					 RGBA8(0,255,0,255), // Colour of text (RGBA)
					 1.0f,               // Text Scale
					 "Hello World!");    // The text that will be displayed
```

# De-Initialisation
Now outside of our main loop, there are still some things we need to add.
```cpp
vita2d_fini();           // De-Initialises Vita2D
vita2d_free_pgf(pgf);    // Frees the font from memory
sceKernelExitProcess(0); // Safley exits the program.
return 0;
```

[Your source code should look like this!](https://docs.pipewarp.co.uk/vita-docs/chapter-2/part-1/main.cpp)

# Part 2: Customising your VPK
Open your Makfile in your text editor. Here, we can customise what the name of the app is, what ID it has and more.
```
TITLE_ID = MYAPP1234
TARGET   = MyApp
```
The title id is the ID of the App in your vita. So when you install the app, and you head over to ux0:app/, your app will be inside the folder with your title_id. Title_ID's **must** be 9 characters long.


Target is the name of the app (what you see on the live area), so it can be anything.

# Part 3: Building
Exit your text editor, and run ```make``` (make sure to run make in the same directory as your makefile!)
Wait a few minutes, and you will have a .vpk in front of you, ready to be installed!

Next part will focus on some more features, like drawing shapes.
