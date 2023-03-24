<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>

</p>

Now that you have an application that can search the music database, return a song and show its audio features data, the next step is to **label** that song’s data in your model with your playlist names from Stage 1. This labelling of data is called **classification**.

![Image showing four labels for the classes in a machine learning model titled reject, mental focus, mood boost and get active](images/labels_wellness.png)

It works like this:

1. You listen to a song and decide if you like it. If you don’t, label it as a `reject`.
2. If you do like it, decide which of your playlists it fits into and label it with that playlist name.

When you label a song’s data and add it to a class, you are sending the audio features values for that song back to your model as **training data**. 

The model doesn’t record the song name, artist or which album it comes from - only the number values of the song’s audio features go into training your model.

![Image showing four classes in a machine learning model, populated with data. They are titled reject, mental focus, mood boost and get active](images/training_data_labeled.png)

As each class in your model collects more data, the model can more accurately predict (guess) other sets of numbers that might fit into a specific class (songs that sound similar). 

You now need to add the part of your program that takes the data for the song you can hear and labels it in your model. Once you have this function working, you will be able to start listening to and classifying loads of new music! 

### Send training data to your model

Your application needs to send labelled song data back to the model, labelling it correctly in each class. To achieve that, each of your sprites will broadcast a message which will then use the grey Machine Learning 4 Kids model blocks to send data back to the model.

When you click on your sprite, it should:
1. Give visual feedback to the user 
2. Send the training data for the current song back to your model on ML4Kids
3. Stop the current song playing
4. Search for a new song to play

First, set up your sprites to broadcast a message when clicked by the user:

--- task ---

Select the icon beneath the Stage for your `reject` sprite.

![Image showing the selected thumbnail for the reject sprite, which is a red X, alongside other sprite thumbnails in scratch](images/reject_thumbnail.png)

**Pro tip:** You can also tell which sprite is selected by checking at the top right of your workspace for the sprite’s costume!

--- /task ---

--- task ---

Click on the Events menu and drag a `broadcast`{:class="block3events"} block into your visual feedback script, making sure it is at the top, beneath the curved `when this sprite clicked`{:class="block3events"} block:

```blocks3
when this sprite clicked
broadcast [Find song v]
next costume
wait (1) seconds
next costume
```

--- /task ---

--- task ---

From the pull-down menu in the block choose New Message:

![](images/classify_broadcast2.png)

--- /task ---

--- task ---

In the pop-up window that appears, type a message which matches your sprite’s name and the class name in your model:
![](images/classify_broadcast3.png)

Your broadcast block will change to show the new message:

```blocks3
when this sprite clicked
broadcast [Reject v]
next costume
wait (1) seconds
next costume
```

--- /task ---

--- task ---

**Repeat** these steps for all of your sprites, making sure that:
+ The message being broadcast matches the name of the sprite **and** 
+ The broadcast happens before the sprite’s visual feedback. (Otherwise it will feel like it’s taking ages to do something!)

--- /task ---

Next, create the scripts which will send the data back to your model. 

--- task ---

Click on the **Stage**. You should see your `Find Song` script in the Workspace.
![](images/select_stage.png)

--- /task ---

--- task ---

From the `Events`{:class="block3events"} menu, add a `when I receive`{:class="block3events"} block and choose `reject` from the pull-down menu:

```blocks3
when I receive [Reject v]
```

--- /task ---

--- task ---

Click on the `ML4Kids` menu - it will be named the same thing as your machine learning model and be at the bottom of the list on the left of your screen:
![](images/ml4k_menu.png)

--- /task ---

You will see a whole list of new grey blocks. These blocks allow you to interact with the machine learning model you created earlier.
![](images/ml4k_blocks.png)

--- task ---

From this list, select the `add training data` block, second from the bottom in the list and add it to the script. It will be quite a long block, as it contains all the values you created in your machine learning model.

![](images/add_training_data.png)

--- collapse ---
---
title: Pro tip - Making more space to work
---

If you need some more room in your workspace, you can:
+ Shrink the stage by clicking the button at the top right 
+ Use the magnifying glass with the negative symbol to zoom out 


--- /collapse ---

--- /task ---
