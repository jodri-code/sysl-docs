# Using Scripts in GameReel

// filler

Create a Node and attach a Mesh to it.

1. Right Click on the Node in the Scene viewer and select `Create Script`.

2. Add a function called `void onKey(GameReel::Key key)`

3. Inside the function write the following

```cpp

void onKey(GameReel::Event gkey){
	switch(gkey::keyPressed){
		case GAMEREEL_KEY_UP:
			GameReelTranslate(id, 0, 1, 0);
			break;
		case GAMEREEL_KEY_DOWN:
			GameReelTranslate(id, 0, 0, 0);
			break;
		case GAMEREEL_KEY_LEFT:
			GameReelTranslate(id, -1, 0, 0);
			break;
		case GAMEREEL_KEY_RIGHT:
			GameReelTranslate(id, 1, 0, 0);
			break;
	}

}
```

4. On the script editor, go into Script Properties and Click on Register Function
5. Type in the function name with type and arguments (argmuents must not have names!) as so:

```cpp
void onKey(int)
```

We have our Movment implemented, but you will get an error when trying to build. This is because there isnt an Update function for our script.
To create one, simply write the following inside the script:

```cpp 
void update(GameReel::Event event){
	onKey(gkey);
}
```

Your game should sucessfully build and you can move your mesh!
