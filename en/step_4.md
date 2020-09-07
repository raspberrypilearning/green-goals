## Affordable and clean energy

Get the **Climate action Panda** to respond to the **Main Panda's** `broadcasts`{:class="block3events"}, creating an action that will help explain the [Climate Action](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-13-climate-action.html) sustainable development goal.

Here is the code you have already. There is some music and some text explaining the **Climate action Panda** goal as well as a script that gets the **Climate action Panda** to `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

![climate action starter code](images/climateaction_startercode.png)

Get the **Climate action Panda** to respond to the **Main Panda's** `broadcast`{:class="block3events"} which you set up in the previous step (Step 2).

--- task ---

Start a new script with the `when backdrop switches to Climate Action`{:class="block3events"} and use a `show`{:class="block3looks"} block to show the **Climate action Panda** on the stage.

![image of the Climate action Panda sprite](images/climateactionpanda-sprite.png)

```blocks3
when backdrop switches to [Climate Action v]
show
```

--- /task ---

--- task ---

Set the size of the **Climate action Panda**.

![image of the Climate action Panda sprite](images/climateactionpanda-sprite.png)

```blocks3
when backdrop switches to (Climate Action v)
+ set size to (50) %
show
```

--- /task ---

In the starter code, you can see a `wait 5 seconds`{:class="block3control"} and that means that the **Climate Action Panda** waits for 5 seconds while the **Main Panda** introduces them.

--- task ---

Get the **Climate Action Panda** to wait 5 seconds before moving as well.

![image of the Climate Action Panda sprite](images/climateactionpanda-sprite.png)

```blocks3
when backdrop switches to (Climate Action v)
set size to (50) %
show
+ wait (5) seconds
```
--- /task ---

--- task ---

Add blocks so that after `waiting 5 seconds`{:class="block3control"}, the **Climate action Panda** gets bigger and smaller.

![image of the Climate action Panda sprite](images/climateactionpanda-sprite.png)

```blocks3
when backdrop switches to (Climate Action v)
set size to (50) %
show
wait (5) seconds
+ repeat (18)
  change size by (5)
  wait (0.2) seconds
  change size by (-5)
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
