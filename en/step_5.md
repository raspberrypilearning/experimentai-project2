## Pick a genre to search

Create the code which will find songs on Spotify, collect their audio features data and play them for you to label in your model.

--- task ---

To get started, delete the cat sprite by clicking the little bin icon on its tile beneath the stage.
![Image showing the scratch cat thumbnail with a picture of a rubbish bin in the top corner](images/delete_sprite.png)

--- /task ---

--- task ---

In the orange `Variables`{:class="block3variables"} menu, select **Make a Variable**.
![](images/make_a_variable.png)

--- /task ---

--- task ---

In the popup, name the new variable genre and select OK.

![](images/genre_make_variable.png)

You will see a few new orange blocks appear in the Variables{:class="block3variables"} menu.

--- /task ---

--- task ---

Select **Make a Variable** again, but name this variable the first of your selected audio features from earlier.

![](images/acoustic_make_variable.png)

Select **OK**.

--- /task ---

--- task ---

**Repeat these steps** until your have a variable block for all of your chosen audio features and one for genre:
![Image showing a list of orange variable blocks](images/variables_list.png)
All of the variables you create will have their blue box ticked by default. This means that they are being displayed with a readout on the stage.

--- collapse ---
---
title: Pro tip - Seeing or hiding variables
---

+ Unticking the blue box next to each variable will hide the readout for that variable on the Stage. 
+ You can set the readout style for each variable by double-clicking it on the stage.

--- /collapse ---

--- /task ---

Now that you have all the extensions and variables you need ready to code, you can start making a program to classify your songs. 

To do this, you need to get Scratch to search for a song in one of your genres and play it so you can listen to it. 

--- task ---

Add a `when green flag clicked`{:class="block3events"} block to your workspace. This is the script that will run the first time we start the project. 

```blocks3
when green flag clicked
```

--- /task ---

--- task ---

In the blue `Sensing`{:class="block3sensing"}  menu, add an `ask (What's your name?) and wait`{:class="block3sensing"} block:

```blocks3
when green flag clicked
ask (What's your name?) and wait
```

--- /task ---

--- task ---

Change the question text to something you like. Ask your user to enter a genre, to start the search. You could say something like:
+ What genre would you like?
+ What are we listening to today?
+ Enter music genre to start!
+ What kind of music do you want to hear?

```blocks3
when green flag clicked
ask (What genre do you want?) and wait
```

--- /task ---

--- task ---

In the orange `Variables`{:class="blocks3variables"} menu, add a `set [genre] to (0)`{:class="blocks3variables"} block, and make sure the pull-down menu in the block is set to **genre**.

```blocks3
when green flag clicked
ask (What genre do you want?) and wait
set [genre] to (0)
```

--- /task ---

--- task ---

Back in the blue `Sensing`{:class="blocks3sensing"} menu, drag the round blue `answer`{:class="blocks3sensing"} bubble across and place it in the hole in the set [genre] to (0) block, replacing the 0:

```blocks3
when green flag clicked
ask (What genre do you want?) and wait
set [genre] to (answer)
```

--- /task ---

--- task ---

**Click the green flag.**

Your script will run, and a prompt will appear, asking you what genre of music you want.

--- /task ---

--- task ---

**Type** something into the prompt and press **Enter**.

You should see your genre readout in the stage change to what you just typed. 

--- collapse ---
---
title: Pro Tip - getting the right genre
---

You can only use genres that the music database recognises in the answer field. If you enter something it doesn’t recognise, your program won’t play any music. (That includes bad spelling and typos!)

--- /collapse ---

--- /task ---

In the next step, you will use the green Spotify blocks to search the online music database for songs to label. 
