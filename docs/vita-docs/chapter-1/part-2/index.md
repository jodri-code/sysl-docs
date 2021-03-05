## [PSVita Guide Index](https://docs.pipewarp.co.uk/vita-docs)

# Part 2: Setting up VitaSDK
###### ez



# Part 1: What is VitaSDK?
Exactly what you think it is, a SDK (software development kit) for creating homebrew on the vita. 



# Part 2: How do I get it?

Follow the steps at https://vitasdk.org/

However, if you still somehow don't get what to do, Here is a detailed guide below.

1.Inside of your Linux terminal (or WSL), type in ```apt-get install make git-core cmake python```
  This will install Python to your terminal, allowing you to run the VitaSDK install script
  

2.Run ```nano .bashrc``` on your terminal. If you have trouble opening it, google a guide on opening this file.

3.Scroll to the bottom of the whole text (make sure to not delete anything!) and once you reach the end, paste in the following:
```
export VITASDK=/usr/local/vitasdk
export PATH=$VITASDK/bin:$PATH # add vitasdk tool to $PATH
```

4.Press Ctrl+S and Ctrl+X

5.Run the following commands in order:
```
git clone https://github.com/vitasdk/vdpm
cd vdpm
./bootstrap-vitasdk.sh
./install-all.sh
```
This will clone the VitaSDK Installation scripts (vdpm) onto your computer and run them.

After the lengthy install, you will have sucessfully installed VitaSDK!
