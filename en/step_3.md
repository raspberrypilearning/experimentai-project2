## Add values to your model

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Set the values in your new project. You’ll need to add a new value each time and make sure each value is a number.
</div>
</div>

--- task ---

Select Add a Value
![Image of a blue button which reads Add a Value](images/add_value.png)

--- /task ---

--- task ---

Enter the name of the first value from your list and set the **Type of value** to **number**
![an image showing two text fields. The field Value 1 is filled with the word acousticness. The field type of value is filled with the word number](images/value_example.png)
--- /task ---

--- task ---

Repeat for all of the audio features in your list, making sure they are all **number** values.

--- /task ---

--- task ---

When you have added all your audio features and checked them, click Create.
![An image of a blue button which reads Create](images/create_button.png)

--- /task ---

Amazing! Your model is now ready to receive **values**, but it’s missing one important thing - **labels**.

**Labels** are how the model recognises the different **classes** we will use to group our songs: our playlist names from the previous stage. While the model is tracking all the audio features of a song, the user labels that data and places it in a class based on whether they think it belongs there. 

For example, if you’re listening to a song that you define as a `heartbreak` track, you need to take all the information about it (the values) and label that data with `heartbreak`**.** This puts it into the `heartbreak` class. Once the model groups the data in this way, it can analyse it and then make predictions based on it.

![An image explainng that a class is a category that data can be assigned to with a picture of several different apples in a box, alongside an explanation that a label is applied to a single piece of data to indicate which class it belongs to and a single apple](images/class_vs_label.png)

The classes you choose could be for times in your user’s life when they might want specific kinds of music playing, or for specific audio features for the model to prefer or avoid. You could have classes for relaxation, mental focus, or getting physically active just as easily as playlists for quiet, loud or live performances. 

--- task ---

**Choose: Pick at least three classes for your model which represent your playlists**

Write them down somewhere - you'll need them later.

--- /task ---

## Add Labels to your model

--- task ---

Click the name of your project on your projects page
![An image showing the project name MusicWellness recognising numbers](images/model_name.png)

--- /task ---

--- task ---

Select **Train**
![An image showing a Button reading Train, and the explanation 'Collect examples of what you want the computer to recognise'](images/train.png)
--- /task ---

--- task ---

Select Add new label and create a label called `reject`. 
This is what we will label any songs we don’t like.
![An image showing a new label called reject being added to a text field](images/reject_label.png)

--- /task ---

--- task ---

Select **Add new label** and create a label for the first playlist name in your list.
![An image showing a button which reads Add new label](images/new_label.png)

--- /task ---

--- task ---

Repeat this step to create labels for each of your playlist names.
![An image showing a new label called break_up being added to a text field](images/break_up_label.png)


As you add them, they will appear as boxes in your model’s training page, ready to receive data.
![An image showing an empty box titled break_up](images/label_box.png)

--- /task ---

--- task ---

When you have added a label for each playlist, select **Back to project**.
![An image showing link text reading Back to project](images/back_to_project.png)

--- /task ---

In the next step, you'll start coding the application to train your model in Scratch!