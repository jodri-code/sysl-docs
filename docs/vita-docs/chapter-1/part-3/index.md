## [PSVita Guide Index](https://docs.pipewarp.co.uk/vita-docs)

# Part 3: Building an App
### help i cant make a hello world


# Part 1: How do I even make a program?
Linux uses Makefiles to configure build projects. This contain information like what compiler to use, what libraries to compile with and what the Apps name will even be!

# Optional: Can I use C++?
Of course! [Refer to this guide.](https://docs.pipewarp.co.uk/vita-docs/not-finished)

# Part 2: How do I get started?

We can clone xerpi's LibVita2D example for a base Makefile and very basic app to get started with.
Run the following commands to download and build it!
```
git clone https://github.com/xerpi/libvita2d
cd libvita2d
cd sample
make
```
Thats it! There should be a .VPK in the same directory!

You can snoop around in the soruce code to get an idea of how the program works.

The next chapter will dicuss how to actually *write* code and learn what all these commands mean.
