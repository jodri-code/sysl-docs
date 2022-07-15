# [SYSlang Docs - Making a GUI: The operations](https://jodri-code.github.io/sysl-docs/SYSlang/#index)

_You must complete [Part 1](https://jodri-code.github.io/sysl-docs/SYSlang/tutorials/GUI1) in order to follow this tutorial_

Where did we leave off?

Oh yeah, Translators...

## Part 1: nogui's rules
To continue in this tutorial, you will need to add `lang requisit == nogui;`

This is our current code, including this change:
```
require monitor;

lang-imp test_V;

from test_V enter GUIs;

lang requisit == nogui;

for translators(C, JS, C#, CPP, Ruby, Py, Java, LUA){
    dl(from('systemware.ga/trans/') enter all).to('A:/')
}
```

This line of code will come in essential in future versions of the OS (avoids a 40-something line work-around)

## Part 2: Internal/External Operations
I'm only going to say it **once**, _don't_ use Internal Operations in your GUI.
Keep everything neat in the main file instead.

To create an External Operation, use a `for` loop. Yes, I did just say that.

For the sake of this tutorials simplicity, I will only add one External Operation, the main GUI. In my case I will simply call it gui, but you can call it whatever you want.

Please note that whatever you call your External Operator's `for` loop will be the name of the command to use said Operator.
```
require monitor;

lang-imp test_V;

from test_V enter GUIs;

lang requisit == nogui;

for translators(C, JS, C#, CPP, Ruby, Py, Java, LUA){
    dl(from('systemware.ga/trans/') enter all).to('A:/')
}

for gui{

}
```

Inside this for loop we need to define what its's `for`. _srry for bad jokes it's like 2:30am_

The first thing we're going to want to call is `nougi.close('this')`

Followed by a `uses('/directory/')` Reference

And ended by a function used only by GUI's; `GUI.open('GUI_in_directory')`
```
require monitor;

lang-imp test_V;

from test_V enter GUIs;

lang requisit == nogui;

for translators(C, JS, C#, CPP, Ruby, Py, Java, LUA){
    dl(from('systemware.ga/trans/') enter all).to('A:/')
}

for gui{
    nogui.close('this');
    uses('./gui/');
    GUI.open('gui');
}
```

For simplicity's sake, everything is labeled as one, but you can totally call the folder `help` and the file `not4u` and it'll work.

## Part 3: The Operation
This is still a work in progress.

There are at least two ways to go about this, so I am working out the best method...
```
require monitor;

lang-imp SYS_IMP_AI;
lang-imp SYSlang_testV;

from SYSlang_testV enter GUIs;
from SYS_IMP_AI enter all;

dl(from(systemware.ga/testGUIs/) enter GUI1).to('A:/');
exe('A:/GUI1.jar');

await(user.res);
```

### [Go Back](https://jodri-code.github.io/sysl-docs/SYSlang/#index)
### [I Want Moar!](https://jodri-code.github.io/sysl-docs/SYSlang/tutorials/GUI3)
