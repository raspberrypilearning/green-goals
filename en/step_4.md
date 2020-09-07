## Affordable and clean energy

Get the **Energy Panda** to respond to the **Main Panda's** `broadcasts`{:class="block3events"}, creating an action that will help explain the [Affordable and clean energy](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-7-affordable-and-clean-energy.html) sustainable development goal.

Just like in the last step, there is some code here with some music and some text explaining the Affordable and clean energy goal as well as a script that gets the **Energy Panda** to `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

Get the **Energy Panda** to respond to the **Main Panda's** `broadcast`{:class="block3events"}.

--- task ---

Start a new script with the `when backdrop switches to Affordable and clean energy`{:class="block3events"} block and use a `show`{:class="block3looks"} block to show the **Energy Panda** on the stage.

![image of the Energy Panda sprite](images/energypanda-sprite.png)

```blocks3
when backdrop switches to [Affordable and clean energy v]
show
```

--- /task ---

--- task ---

Get the **Energy Panda** to point in the other direction so it is interacting with the **Main Panda**

![image of the Energy Panda sprite](images/energypanda-sprite.png)

```blocks3
when backdrop switches to (Affordable and clean energy v)
+ point in direction (90)
show
```

--- /task ---

--- task ---

Get the **Energy Panda** to wait 5 seconds for the **Main Panda's** introduction before moving.

![image of the Energy Panda sprite](images/energypanda-sprite.png)

```blocks3
when backdrop switches to (Affordable and clean energy v)
point in direction (90)
show
+ wait (5) seconds
```
--- /task ---

--- task ---

Add blocks so that after `waiting 5 seconds`{:class="block3control"}, the **Energy Panda** moves from side to side.

![image of the Energy Panda sprite](images/energypanda-sprite.png)

```blocks3
when backdrop switches to (Affordable and clean energy v)
set size to (50) %
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

Get the **Climate action Panda** to respond to the next `broadcast`{:class="block3events"} from the **Main Panda** and `hide`{:class="block3looks"} when it is finished explaining its goal.

--- task ---

Start a new script with the `when I recieve next`{:class="block3events"} and `hide`{:class="block3looks"} blocks.

![image of the Climate action Panda sprite](images/climateactionpanda-sprite.png)

```blocks3
when I receive [next v]
hide
```

--- /task ---

--- save ---
