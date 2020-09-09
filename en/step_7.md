## Life on land

Get the **Land Panda** sprite to respond to the United Nations' Sustainable Development Goal, [Life on Land](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-15-life-on-land.html){:target="_blank"}, with a specfic action, sound and setting.

--- task ---

Go to the **Code** tab for the **Land Panda**.

You will see some code already provided for you. The code includes music and text explaining the Life on Land goal as well as a script that gets the **Land Panda** sprite to `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

--- /task ---

Get the **Land Panda** sprite to respond to the `broadcast`{:class="block3events"} in the **Main Panda** sprite.

--- task ---

Add a  `when backdrop switches to Life on Land`{:class="block3events"} block and use a `show`{:class="block3looks"} block to show the **Land Panda** sprite on the stage:

![image of the Land Panda sprite](images/landpanda-sprite.png)

```blocks3
when backdrop switches to [Life on Land v]
show
```

--- /task ---

Change the size of the **Land Panda** sprite.

--- task ---

Reduce the size of the **Land Panda** sprite by adding a `set size to`{:class="block3looks"} block and change the value to `50` percent:

![image of the Land Panda sprite](images/landpanda-sprite.png)

```blocks3
when backdrop switches to (Life on Land v)
+ set size to (50) %
show
```

--- /task ---

Before it moves, get the **Land Panda** sprite to wait to be introduced by the **Main Panda**.

--- task ---

Add a `wait`{:class="block3looks"} block and change its value to `5` seconds:

![image of the Land Panda sprite](images/landpanda-sprite.png)

```blocks3
when backdrop switches to (Life on Land v)
set size to (50)%
show
+ wait (5) seconds
```
--- /task ---

Now the **Land Panda** sprite needs to jump up and down.

--- task ---

Add in a `repeat`{:class="block3control"} block and within it the following: 

`change y by`{:class="block3motion"} block with a value of `10` (so **Land Panda** sprite goes up)
`wait`{:class="block3control"} block (to slow down **Land Panda**'s action)
`change y by`{:class="block3motion"} block with a value of `-10` (so **Land Panda** sprite goes down)
`wait`{:class="block3control"} block (to slow down **Land Panda**'s action)

![image of the Land Panda sprite](images/landpanda-sprite.png)

```blocks3
when backdrop switches to (Life on Land v)
set size to (50)%
show
wait (5) seconds
+ repeat (18)
  change y by (10)
  wait (0.2) seconds
  change y by (-10)
  wait (0.2) seconds
end
```

--- /task ---

Get the **Land Panda** sprite to respond to the next `broadcast`{:class="block3events"} from the **Main Panda** sprite and `hide`{:class="block3looks"} when it is finished explaining its goal.

--- task ---

Start a new script with the `when I receive next`{:class="block3events"} and `hide`{:class="block3looks"} blocks.

![image of the Land Panda sprite](images/landpanda-sprite.png)

```blocks3
when I receive [next v]
hide
```

--- /task ---

--- task ---

Now test your program with the new sprite and backdrop.

--- /task ---

--- save ---
