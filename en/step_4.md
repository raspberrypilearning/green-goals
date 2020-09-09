## Affordable and clean energy

Get the **Climate Panda** sprite to respond to the United Nations' Sustainable Development Goal, [Affordable and clean energy](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-7-affordable-and-clean-energy.html), with a specfic action, sound and setting.

As with the previous step, there is some code here with some music and some text explaining the Affordable and clean energy goal as well as a script that gets the **Energy Panda** sprite to `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

Get the **Energy Panda** sprite to respond to the **Main Panda** sprite's `broadcast`{:class="block3events"}.

--- task ---

Go to the Code tab for the **Energy Panda** sprite.

--- /task ---

--- task ---

Add a `when backdrop switches to Affordable and clean energy`{:class="block3events"} block and use a `show`{:class="block3looks"} block to show the **Energy Panda** sprite on the stage:

![image of the Energy Panda sprite](images/energypanda-sprite.png)

```blocks3
when backdrop switches to [Affordable and clean energy v]
show
```

--- /task ---

--- task ---

Add a `point in direction block`{:class="block3motion"} so that the **Energy Panda** sprite faces right so it appears to interact with the **Main Panda** sprite:

![image of the Energy Panda sprite](images/energypanda-sprite.png)

```blocks3
when backdrop switches to (Affordable and clean energy v)
+ point in direction (90)
show
```

--- /task ---

The **Energy Panda** sprite needs to wait for the **Main Panda** sprite to introduce the Green Goal.

--- task ---

Add a `wait 5 seconds`{:class="block3control"} block:

![image of the Energy Panda sprite](images/energypanda-sprite.png)

```blocks3
when backdrop switches to (Affordable and clean energy v)
point in direction (90)
show
+ wait (5) seconds
```
--- /task ---

We now want **Energy Panda** sprite to respond by moving from side to side.
--- task ---

Use the following blocks to do this: `turn right`{:class="block3motion"} `15` degrees, `wait 0.2 seconds`{:class="block3control"}, `turn left`{:class="block3motion"} `15` degrees and `wait 0.2 seconds`{:class="block3control"}:

![image of the Energy Panda sprite](images/energypanda-sprite.png)

```blocks3
when backdrop switches to (Affordable and clean energy v)
point in direction (90) %
show
wait (5) seconds
+ repeat (18)
  turn right (15) degrees
  wait (0.2) seconds
  turn left (15) degrees
  wait (0.2) seconds
end
```

--- /task ---

Get the **Energy Panda** sprite to respond to the next `broadcast`{:class="block3events"} from the **Main Panda** sprite and `hide`{:class="block3looks"} when it is finished explaining its goal.

--- task ---

Start a new script with the `when I receive next`{:class="block3events"} and `hide`{:class="block3looks"} blocks:

![image of the Energy Panda sprite](images/climateactionpanda-sprite.png)

```blocks3
when I receive [next v]
hide
```

--- /task ---

--- save ---
