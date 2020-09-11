## Walk through the goals

In this step you will program the **Main Panda** sprite to walk from the left to the right-hand side of the stage, changing to the next backdrop when it reaches the right-hand side of the stage. A message is then broadcast to let all the sprites know when the backdrop changes.

--- task ---

**Online:** open the [starter project](http://rpf.io/p/en/green-goals-on){:target="\_blank"} in Scratch.

**Offline:** open the project [starter file](http://rpf.io/p/en/green-goals-get){:target="\_blank"} in the Scratch offline editor. If you need to download and install Scratch, you can find it [here](https://scratch.mit.edu/download){:target="\_blank"}.

The Scratch environment that you will open looks like this:

![starter project](images/starterproject.png)

--- /task ---

In this step you will be programming the **Main Panda** sprite to walk through each of the five Green Goal backdrops.

You will be using the `Broadcast`{:class="block3events"} blocks which are messages that are sent by a sprite for some or all other sprites to receive. You'll be familiar with `Broadcasts`{:class="block3events"} if you completed the [Focus on the prize](https://learning-admin.raspberrypi.org/en/projects/focus-on-the-prize){:target="\_blank"} project in the [Look after yourself](https://projects.raspberrypi.org/en/pathways/look-after-yourself){:target="\_blank"} pathway.

A group of blocks joined together is called a script. The **Main Panda** sprite will have two scripts.

--- task ---

The first script will set up the animation sequence. The **Main Panda** will broadcast a message to the sprites. To create the first script, select the following blocks from the `Events`{:class="block3events"} blocks menu: `when green flag clicked`{:class="block3events"} and `broadcast message1`{:class="block3events"}. Click on the dropdown in `broadcast message1`{:class="block3events"} block and select new message then title it 'next':

```blocks3
when green flag clicked
broadcast [next v]
```

--- /task ---

--- task ---

The second script controls the movement of the **Main Panda** sprite across the five different backdrops. To create the second script, go to the `Events`{:class="block3events"} blocks menu and select `when I receive next`{:class="block3events"} block:

```blocks3
when I receive [next v]
```
--- /task ---

--- task ---

Arrange the blocks so that you have two scripts.

![screenshot of the two scripts side by side](images/broadcast-scripts.png)

--- /task ---

Now you need to get the **Main Panda** sprite to enter from the bottom left-hand corner.

--- task ---

From the `Motion`{:class="block3motion"} block menu, add a `go to x:() y:()`{:class="block3motion"} block. Change the coordinates to x: `-168` and y: `-87`:

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when I receive [next v]
+ go to x: (-168) y: (-87)
```

--- /task ---

The **Main Panda** sprite needs to show at the beginning and hide at the end.

--- task ---

To do this, go to the `Looks`{:class="block3looks"} menu and add the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks. (In the next task you will put some more code between the show and hide):

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when I receive [next v]
go to x: (-168) y: (-87)
+show
+hide
```
--- /task ---

Get the **Main Panda** sprite to move across the left tothe right-hand side of the stage until it touches the edge.

--- task ---

To do this, add the following blocks: `repeat`{:class="block3control"} loop that repeats `move 10 steps`{:class="block3motion"} until the sprite is `touching edge`{:class="block3sensing"}:

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when I receive [next v]
go to x: (-168) y: (-87)
show
+ repeat until <touching[edge v]>
  move (10) steps
end
hide
```

--- /task ---

--- task ---

Run your program to test it.

--- /task ---

You now need to program the next backdrop to appear when the **Main Panda** reaches the edge of the stage on the right-hand side.

--- task ---
Now add the following two blocks to the end of the script: `broadcast next`{:class="block3events"} and `next backdrop`{:class="block3looks"} blocks:

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when I receive [next v]
go to x: (-168) y: (-87)
show
repeat until <touching[edge v]>
  move (10) steps
end
hide
+ broadcast [next v]
+ next backdrop
```

--- /task ---

Now add the finishing touches. Get the **Main Panda** sprite to introduce the panda for each Green Goal by announcing each Green Goal's **Backdrop** title. And add some wait time so that the Green Goal pandas can explain their goal.

--- task ---
Add a `say backdrop name`{:class="block3looks"} and a `wait`{:class="block3control"} block:

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when I receive [next v]
go to x: (-168) y: (-87)
show
+ say (backdrop [name v]) for (4) seconds
+ wait (12) seconds
repeat until <touching[edge v]>
  move (10) steps
end
hide
broadcast [next v]
next backdrop
```

--- /task ---

You will need to stop the music playing when the **Main Panda** goes to the next Green Goal backdrop.

--- task ---

Add one final block, `stop all sounds`{:class="block3sound"} to the script:

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when I receive [next v]
go to x: (-168) y: (-87)
show
say (backdrop [name v]) for (4) seconds
wait (12) seconds
repeat until <touching[edge v]>
  move (10) steps
end
hide
broadcast [next v]
next backdrop
+ stop all sounds
```
--- /task ---

--- task ---

Run your program to test it. You should see the backdrops show in turn. After the final backdrop, **Life on Land**, the program goes round to the beginning backdrop which is **Climate action**. This is becuase, once the program reaches the final backdrop, the next backdrop command makes it return to the beginning.

--- /task ---

--- save ---
