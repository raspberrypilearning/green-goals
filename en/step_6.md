## Life below water

Get the **Water Panda** sprite to respond to the United Nations' Sustainable Development Goal, [Life Below Water](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-14-life-below-water.html) with a specfic action, sound and setting.

Just like in the last step, there is some code here with some music and some text explaining theLife Below Water goal as well as a script that gets the **Water Panda** sprite to `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

Get the **Water Panda** sprite to respond to the **Main Panda** sprite's `broadcast`{:class="block3events"}.

--- task ---

Start a new script with the `when backdrop switches to Life Below Water`{:class="block3events"} block and use a `show`{:class="block3looks"} block to show the **Water Panda** sprite on the stage.

![image of the Water Panda sprite](images/waterpanda-sprite.png)

```blocks3
when backdrop switches to [Life Below Water v]
show
```

--- /task ---

--- task ---

Get the **Water Panda** sprite to point straight up so we can get it to only move up and down the stage, and only rotate left and right.

![image of the Water Panda sprite](images/waterpanda-sprite.png)

```blocks3
when backdrop switches to (Life Below Water v)
+ point in direction (0)
+ set rotation style [left-right v]
show
```

--- /task ---

--- task ---

Get the **Water Panda** sprite to wait 5 seconds for the **Main Panda** sprite's introduction before moving.

![image of the Water Panda sprite](images/waterpanda-sprite.png)

```blocks3
when backdrop switches to (Life Below Water v)
point in direction (0)
set rotation style [left-right v]
show
+ wait (5) seconds
```
--- /task ---

--- task ---

Add blocks so that after `waiting 5 seconds`{:class="block3control"}, the **Energy Panda** sprite moves up and down the stage.

THIS NEEDS TO BE EXPLAINED MORE.

![image of the Water Panda sprite](images/waterpanda-sprite.png)

```blocks3
when backdrop switches to (Life Below Water v)
point in direction (0)
set rotation style [left-right v]
show
wait (5) seconds
+ repeat until <not <([backdrop # v] of (stage)) = (4)>>S
  move (2) steps
  if on edge, bounce
```

--- /task ---

Get the **Water Panda** sprite to respond to the next `broadcast`{:class="block3events"} from the **Main Panda** sprite and `hide`{:class="block3looks"} when it is finished explaining its goal.

--- task ---

Start a new script with the `when I receive next`{:class="block3events"} and `hide`{:class="block3looks"} blocks.

![image of the Water Panda sprite](images/waterpanda-sprite.png)

```blocks3
when I receive [next v]
hide
```

--- /task ---

--- save ---
