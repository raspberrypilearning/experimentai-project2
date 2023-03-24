## Collect song data

Now that you can search a genre in the music database, you need to be able to send the audio features data to your model. To do that, store each audio feature as the variable you created of the same name.

--- task ---

**Detach** the play preview block from your script. 

You are about to add a lot of blocks to this script, and you don’t want your ears blasted off by accidentally playing music all the time.

```blocks3
when green flag clicked
ask [What genre do you want?] and wait
set [genre] to (answer)
random song from genre (genre) :: #338854

play preview :: #338854
```
--- /task ---

--- task ---

From the `Variables`{:class="blocks3variables"} menu, add a `set [variable] to (0)`{:class="blocks3variables"} block to your script, to the bottom of the `random song from genre (genre)`{:class="blocks3custom"} block.

--- /task ---





--- save ---