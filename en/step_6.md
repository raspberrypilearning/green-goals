## Life Below Water

Get the **Water Panda** sprite to respond to the United Nations' Sustainable Development Goal, [Life Below Water](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-14-life-below-water.html){:target="\_blank"}, with a specfic action, sound and setting.

--- task ---

Go to the **Code** tab for the **Water Panda**.

You will see the code already provided for you, like in the previous steps.

--- /task ---

Get the **Water Panda** sprite to respond to the `broadcast`{:class="block3events"} in the **Main Panda** sprite.

--- collapse ---

Add a  `when backdrop switches to Life Below Water`{:class="block3events"} block and use a `show`{:class="block3looks"} block to show the **Water Panda** sprite on the stage:

![image of the Water Panda sprite](images/waterpanda-sprite.png)

```blocks3
when backdrop switches to [Life Below Water v]
show
```

--- /collapse ---

Get the **Water Panda** sprite to point straight up so it only moves up and down the stage, and only rotates left and right.

--- task ---

Add a `point in direction 90`{:class="block3motion"} block and change the `90` to `0` so that it can move up and down instead of right and left. Add a `set rotation style left-right`{:class="block3motion"} block so that the sprite rotates left and right instead of flipping upside down:

![image of the Water Panda sprite](images/waterpanda-sprite.png)

```blocks3
when backdrop switches to [Life Below Water v]
+ point in direction (0)
+ set rotation style [left-right v]
show
```

--- /task ---

As with the previous Green Goals sprites, **Water Panda** sprite needs to wait to be introduced by the **Main Panda** sprite.

--- collapse ---

Add a `wait`{:class="block3control"} block for `5` seconds:

![image of the Water Panda sprite](images/waterpanda-sprite.png)

```blocks3
when backdrop switches to [Life Below Water v]
point in direction (0)
set rotation style [left-right v]
show
+ wait (5) seconds
```

--- /collapse ---

Get the **Water Panda** sprite to only move when its backdrop shows.

--- task ---

Add a `repeat until`{:class="block3control"} block so that the **Water Panda** sprite does `not`{:class="block3operators"} move unless the `backdrop of stage`{:class="block3sensing"} `=`{:class="block3operators"} `4`. The value 4 stands for the 4th backdrop - Life Below Water:

![image of the Water Panda sprite](images/waterpanda-sprite.png)

```blocks3
when backdrop switches to [Life Below Water v]
point in direction (0)
set rotation style [left-right v]
show
wait (5) seconds
+ repeat until <not <([backdrop # v] of [stage v])= (4)>>
end
```
--- /task ---

You now need to make the  **Water Panda** sprite swim up to the top of the stage and back down again.

--- task ---
To do this add two `Motion`{:class="block3motion"} blocks: `move 2 steps`{:class="block3motion"} and `if on edge, bounce`{:class="block3motion"}:

```blocks3
when backdrop switches to [Life Below Water v]
point in direction (0)
set rotation style [left-right v]
show
wait (5) seconds
repeat until <not <([backdrop v] of [stage v])= (4)>>
+ move (2) steps
+ if on edge, bounce
end
```

--- /task ---

As in previous steps, get the **Water Panda** sprite to respond to the next `broadcast`{:class="block3events"} from the **Main Panda** sprite and `hide`{:class="block3looks"} when it is finished explaining its goal.

--- collapse ---

Start a new script with the `when I receive next`{:class="block3events"} and `hide`{:class="block3looks"} blocks:

![image of the Water Panda sprite](images/waterpanda-sprite.png)

```blocks3
when I receive [next v]
hide
```

--- /collapse ---

--- task ---

Now test your program with the new sprite and backdrop.

--- /task ---

--- save ---
