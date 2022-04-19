# [Making A Login Form](https://systemware.ga/SYSlang/#index)

### *insert dad joke here*
Now that you know some basics, let's get to something more interesting...
A login form

In this tutorial you will learn:
* How to make a script execute on opening
* How `wait.input()` works different to `if(btn(any).this()), optional, optional`
* How to proceed after waiting for input
* How to add a small yet expandable database to your login form, and connect it to your script to  verify the login
* How to change colours of nogui for a more interesting login form (wow that's a mouthful to say)

Let's start, shall we?
## Part 1: The Text Printout

Ok, so this part is going to be one of the longest, because there is no simple way to `print` into the nogui.
```
on(exc){

}
```
This is an on execute loop. Makes the script execute on opening.

In this execute loop, we want to call our method(s) to write the text and input fields into the nogui.
```
on(exc){
 printout1();
 printout2();
 answer1();
 answer2();
}

printout1(txt){
}
printout2(txt){
}
answer1(inf){
}
answer2(inf){
}
```

In my case, I named them in an obvious way. You can name them whatever you like.
We dont need to declare what type the on execute loop is executing, for performance reasons, just type the name.

Next, we add the actual text:
```
on(exc){
 printout1();
 printout2();
 answer1();
 answer2();
}

printout1(txt){
 'User'+cha37&+'Name'
}
printout2(txt){
 'Password'
}
answer1(inf){
}
answer2(inf){
}
```

Notice how when opening this script it will print out username then password then the two input fields?

That's because we ordered them that way in our on execute loop. Rearranging them will fix that.
```
on(exc){
 printout1();
 answer1();
 printout2();
 answer2();
}

printout1(txt){
 'User'+cha37&+'Name'
}
printout2(txt){
 'Password'
}
answer1(inf){
}
answer2(inf){
}
```

That should fix the arrangement problem.

## Part 2: What happens after text is entered

So, what will this code do when you have typed something in the input fields?
Well... nothing. But that's because we didnt code it to do anything.

So let's do that:
```
on(exc){
 printout1();
 answer1();
 printout2();
 answer2();
 login();
}

printout1(txt){
 'User'+cha37&+'Name'
}
printout2(txt){
 'Password'
}
answer1(inf){
}
answer2(inf){
}
login(if(btn(cha38&).this()), answer1(), answer2()){
 clr(nogui.this());
}
```
This will clear the screen if the enter key is pressed, and only if answer1 and answer2 have been filled in.

You could change this to `wait.input(answer1, answer2)`, but that would automatically execute as soon as a single letter has been entered in both fields.
```
on(exc){
 printout1();
 answer1();
 printout2();
 answer2();
 login();
}

printout1(txt){
 'User'+cha37&+'Name'
}
printout2(txt){
 'Password'
}
answer1(inf){
}
answer2(inf){
}
login(if(btn(cha38&).this()), answer1(), answer2()){
 clr(nogui.this()).then(printout3+cha37&+'Welcome');
 printout3(txt){
  answer1().txt();
 }
}
```
And that will print out the username and the word welcome.

## Part 3: Connecting the DB to restrict access

As a side note: this will make a secondary script with usernames and passwords. It's the equivalent to a txt file on windows...
```
on(exc){
 load(data).from(./dbuf/);
 printout1();
 answer1();
 printout2();
 answer2();
 login();
}

data(dbuf){
}
printout1(txt){
 'User'+cha37&+'Name'
}
printout2(txt){
 'Password'
}
answer1(inf){
}
answer2(inf){
}
login(if(btn(cha38&).this()), answer1(), answer2()){
 clr(nogui.this()).then(printout3+cha37&+'Welcome');
 printout3(txt){
  answer1().txt();
 }
}
```
I recommend running the script at this point, so it makes the username and password file correctly. 
```
on(exc){
 load(data).from(./dbuf/);
 printout1();
 answer1();
 printout2();
 answer2();
 login();
}

data(dbuf){
}
printout1(txt){
 'User'+cha37&+'Name'
}
printout2(txt){
 'Password'
}
answer1(inf){
}
answer2(inf){
}
login(if(btn(cha38&).this()), answer1(), answer2()){
 on(login){
  data(dbuf).add(answer1().txt, answer2().txt).ch(if{
  data.exist(login)}
  else{data.add.format(dbuf)}
  )
 }
 clr(nogui.this()).then(printout3+cha37&+'Welcome');
 printout3(txt){
  answer1().txt();
 }
}
```
And there you have it, one fully functional login form connected to a simple database.
Please note, this will login to existing accounts if the username and password coincide, if not, it will create a new user (if the username already exists it will just reload the script)

**Passwords cannot be changed once set in this script!**

## [Return, because my head is working up a storm](https://systemware.ga/SYSlang/#index)
