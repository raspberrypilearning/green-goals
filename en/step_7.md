## Life on land

Get the **Land Panda** sprite to respond to the United Nations' Sustainable Development Goal, [Life on Land](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-15-life-on-land.html) with a specfic action, sound and setting.

Just like in the last step, there is some code here with some music and some text explaining theLife Below Water goal as well as a script that gets the **Land Panda** sprite to `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

Get the **Land Panda** sprite to respond to the **Main Panda** sprite's `broadcast`{:class="block3events"}.

--- task ---

Start a new script with the `when backdrop switches to Life on Land`{:class="block3events"} block and use a `show`{:class="block3looks"} block to show the **Land Panda** sprite on the stage.

![image of the Land Panda sprite](images/landpanda-sprite.png)

```blocks3
when backdrop switches to [Life on Land v]
show
```

--- /task ---

--- task ---

Set the size of the **Land Panda** sprite.

![image of the Land Panda sprite](images/landpanda-sprite.png)

```blocks3
when backdrop switches to (Life on Land v)
+ set size to (50) %
show
```

--- /task ---

--- task ---

Get the **Land Panda** sprite to wait 5 seconds for the **Main Panda** sprite's introduction before moving.

![image of the Land Panda sprite](images/landpanda-sprite.png)

```blocks3
when backdrop switches to (Life on Land v)
set size to (50)%
show
+ wait (5) seconds
```
--- /task ---

--- task ---

Add blocks so that the **Land Panda** sprite jumps up and down.

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

--- save ---
