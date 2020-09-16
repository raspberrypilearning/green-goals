## Walk through the goals

In this step, you will write the program for the **Main Panda** sprite. In this program, the **Main Panda** sprite will walk from the left-hand side of the Stage to the right-hand side, then it will change the backdrop, and broadcast a message to let all the sprites know when the backdrop changes.

--- task ---

**Online:** open the [starter project](http://rpf.io/green-goals-on){:target="\_blank"} in Scratch.

**Offline:** open the [project starter file](http://rpf.io/p/en/green-goals-get){:target="\_blank"} in the Scratch offline editor. If you need to, you can [download and install Scratch here](https://scratch.mit.edu/download){:target="\_blank"}.

The Scratch environment that you will open looks like this:

![starter project](images/starterproject.png)

--- /task ---

In this step, you will program the **Main Panda** sprite to walk through five different backdrops.

You will use the `broadcast`{:class="block3events"} blocks, which are messages that are sent by a sprite for some or all other sprites to receive. If you have completed the [Focus on the prize](https://learning-admin.raspberrypi.org/en/projects/focus-on-the-prize){:target="\_blank"} project in the [Look after yourself](https://projects.raspberrypi.org/en/pathways/look-after-yourself){:target="\_blank"} pathway, you will be familiar with `broadcast`{:class="block3events"} blocks.

A group of blocks joined together is called a 'script'. The **Main Panda** sprite will have two scripts.

--- task ---

The first script will set up the animation sequence. The **Main Panda** sprite will broadcast a message to the sprites. To create the first script, select the following blocks from the `Events`{:class="block3events"} blocks menu: `when green flag clicked`{:class="block3events"} and `broadcast message1`{:class="block3events"}. Click on the drop-down menu in the `broadcast message1`{:class="block3events"} block and select **New message**, then give it the title `next`:

```blocks3
when green flag clicked
broadcast [next v]
```

--- /task ---

--- task ---

The second script will control the movement of the **Main Panda** sprite across the five different backdrops. To create the second script, go to the `Events`{:class="block3events"} blocks menu and select the `when I receive next`{:class="block3events"} block:

```blocks3
when I receive [next v]
```
Arrange the blocks so that you have two scripts.

![screenshot of the two scripts side by side](images/broadcast-scripts.png)

--- /task ---

Now, you need to program the **Main Panda** sprite to enter from the bottom left-hand corner.

--- task ---

From the `Motion`{:class="block3motion"} blocks menu, add a `go to x: y:`{:class="block3motion"} block under the `when I receive next`{:class="block3events"} block. Change the coordinates to `x:`{:class="block3motion"} `-168` and `y:`{:class="block3motion"} `-87`:

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when I receive [next v]
+ go to x: (-168) y: (-87)
```

--- /task ---

The **Main Panda** sprite needs to show at the beginning and hide at the end.

--- task ---

First, go to the `Looks`{:class="block3looks"} blocks menu and add the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks to your program. In the next task, you will put some more code between the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks.

![image of the main Panda sprite](images/mainpanda-sprite.png)

```blocks3
when I receive [next v]
go to x: (-168) y: (-87)
+show
+hide
```
--- /task ---

Now, you need to program the **Main Panda** sprite to move from the left-hand side of the Stage to the right-hand side, until it touches the edge.

--- task ---

To do this, add a `repeat until`{:class="block3control"} loop that repeats `move 10 steps`{:class="block3motion"} until the sprite is `touching edge`{:class="block3sensing"}:

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

You now need to program the next backdrop to appear when the **Main Panda** sprite reaches the edge of the Stage on the right-hand side.

--- task ---
Add the following two blocks to the end of the script: `broadcast next`{:class="block3events"} and `next backdrop`{:class="block3looks"}:

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

Now, add the finishing touches. To introduce the panda for each Green Goal, the **Main Panda** sprite needs to announce each **backdrop** title. You also need to allow some time so that the pandas can explain their Green Goals.

--- task ---
Add a `say backdrop name for 2 seconds`{:class="block3looks"} block and change the value to `4` (seconds). Also, add a `wait`{:class="block3control"} block and set the value to `12` (seconds):

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

Finally, you need to stop the music playing when the **Main Panda** goes to the next backdrop.

--- task ---

Add one final block, `stop all sounds`{:class="block3sound"}, to the script:

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

Run your program to test it. You should see the backdrops show in turn. After the final backdrop, **Life on Land**, the program goes back to the first backdrop, which is **Climate action**. This is because once the program reaches the final backdrop, the `next backdrop`{:class="block3looks"} command makes it return to the beginning.

--- /task ---

--- save ---
