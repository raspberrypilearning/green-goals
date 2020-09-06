## Walk through the goals

Get the UN panda to walk through the different Green Goals, making the Green Goal Panda sprites respond to the backdrop changes.

--- task ---

**Online:** open the [starter project](http://rpf.io/p/en/projectName-on){:target="_blank"} in Scratch.

**Offline:** open the project [starter file](http://rpf.io/p/en/projectName-get){:target="_blank"} in the Scratch offline editor. If you need to download and install Scratch, you can find it [here](https://scratch.mit.edu/download){:target="_blank"}.

The Scratch environment that you will open looks like this:

![starter project](images/starter_project.png)

--- /task ---

In this project, there is one **Main Panda** sprite that walks through the UN Sustainable Development Goals (Green Goals) and introduces the other pandas. Each Green Goal has its own Panda sprite and its own backdrop.

[[picture/screenshot? pandas and backdrops]]

You will be programming the **Main Panda** sprite to walk through each of the 5 backdrops representing the Green Goals.

--- no-print ---
Watch this short video, which shows what to do next.

![screenshot](images/NOTNAMEDYET.gif)

Now follow each task given below.
--- /no-print ---

As you may remember if you've done the Focus on the Prize project, **Broadcasts** are messages that are sent by a sprite for some or all other sprites to receive.

In the `Events`{:class="block3events"} blocks menu, select the `broadcast`{:class="block3events"}, `broadcast next`{:class="block3events"}, and `whenflagclicked`{:class="block3events"} blocks

--- task ---

Arrange the blocks so that you have two scripts, one for setting up the animation sequence for the backdrops, and the other for the **Main Panda** sprite, which continues the animation through the Green Goals.

![screenshot of the two scripts side by side](images/broadcast-scripts.png)

--- /task ---

Get the **Main Panda** sprite to start from the bottom left corner.

--- task ---

Add a `go to x:() y:()`{:class="block3motion"} block from the `Motion`{:class="block3motion"} menu and change the coordinates to x: `-168` and y: `-87`.

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when I receive [next v]
+ go to x: (-168) y: (-87)
```

--- /task ---

Show the **Main Panda** sprite at the beginning of each Green Goal, and hide it at the end.

--- task ---

Go to the `Looks`{:class="block3looks"} menu and add the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks

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

Add a `repeat`{:class="block3control"} loop with a `Sensing`{:class="block3sensing"} condition that repeats `move (10) steps`{:class="block3motion"} until the sprite is `touching(edge)`{:class="block3sensing"}.

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

When the **Main Panda** reaches the edge of the stage, program the next backdrop to appear.

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

Uh oh, the Main Panda disappears when it gets to the [[NEXT?]] backdrop!

[[GIF HERE?]]

Make sure the Main Panda is at the front of all the backdrop layers.

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

Add the finishing touches. Get the Main Panda to introduce the panda for each Green Goal, and add some waiting time to let the Green Goal pandas explain their goals.

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
