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
