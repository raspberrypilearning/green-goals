## Walk through the goals

Get the United Nations' panda, the **Main Panda** sprite, to introduce the five Green Goals. The **Main Panda** sprite will walk through a different backdrop for each goal and there, in the related scene, will be a unique Green Goal Panda sprite who will explain the goal with action, sounds and words.

--- task ---

**Online:** open the [starter project](http://rpf.io/p/en/projectName-on){:target="_blank"} in Scratch.

**Offline:** open the project [starter file](http://rpf.io/p/en/projectName-get){:target="_blank"} in the Scratch offline editor. If you need to download and install Scratch, you can find it [here](https://scratch.mit.edu/download){:target="_blank"}.

The Scratch environment that you will open looks like this:

![starter project](images/starter_project.png)

--- /task ---

You will be programming the **Main Panda** sprite to walk through each of the five Green Goal backdrops.

[[picture/screenshot? pandas and backdrops]]

--- task ---

--- no-print ---
Watch this short video, which shows what to do next.

![screenshot](images/NOTNAMEDYET.gif)

--- /no-print ---
--- /task ---
Now follow each task given below.

You will be using the `Broadcast`{:class="block3events"} blocks which are messages that are sent by a sprite for some or all other sprites to receive. You'll be familiar with `Broadcasts`{:class="block3events"} if you completed the [Focus on the Prize](https://learning-admin.raspberrypi.org/en/projects/focus-on-the-prize) project in the [Look after yourself](https://projects.raspberrypi.org/en/pathways/look-after-yourself) pathway.

--- task ---

In the `Events`{:class="block3events"} menu, select the following blocks: `broadcast`{:class="block3events"}, `broadcast next`{:class="block3events"}, and `when green flag clicked`{:class="block3events"} blocks.

--- /task ---

--- task ---

Arrange the blocks so that you have two scripts, one for setting up the animation sequence for the backdrops, and the other for the **Main Panda** sprite, which continues the animation through the five green goals.

![screenshot of the two scripts side by side](images/broadcast-scripts.png)

--- /task ---

Get the **Main Panda** sprite to enter from the bottom left-hand corner.

--- task ---

From the `Motion`{:class="block3motion"} menu, add a `go to x:() y:()`{:class="block3motion"} block. Change the coordinates to x: `-168` and y: `-87`:

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when I receive [next v]
+ go to x: (-168) y: (-87)
```

--- /task ---

Show the **Main Panda** sprite at the beginning and hide it at the end.

--- task ---

Go to the `Looks`{:class="block3looks"} menu and add the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks:

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when flag clicked
go to x: (-168) y: (-87)
+show
+hide
```

--- /task ---

Get the **Main Panda** sprite to move across the stage until it touches the edge of the stage.

--- task ---

Add a `repeat`{:class="block3control"} loop with a `Sensing`{:class="block3sensing"} condition that repeats `move (10) steps`{:class="block3motion"} until the sprite is `touching(edge)`{:class="block3sensing"}:

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when flag clicked
go to x: (-168) y: (-87)
show
+ repeat until <touching[edge v]>
  move (10) steps
end
hide
```

--- /task ---

You now need to program the next backdrop to appear when the **Main Panda** reaches the edge of the stage.

--- task ---

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when flag clicked
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

Uh oh, the **Main Panda** disappears when it gets to the [[NEXT?]] backdrop!

[[GIF HERE?]]

Make sure the **Main Panda** is at the front of all the backdrop layers.

--- task ---

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when flag clicked
go to x: (-168) y: (-87)
show
+ go to [front v] layer
repeat until <touching[edge v]>
  move (10) steps
end
hide
broadcast [next v]
next backdrop
```

--- /task ---

Add the finishing touches. Get the Main Panda to introduce the panda for each Green Goal by annoncuing their **Backdrop** title. And add some waiting time to let the Green Goal pandas explain their goals.

--- task ---

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when flag clicked
go to x: (-168) y: (-87)
show
go to [front v] layer
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

--- save ---
