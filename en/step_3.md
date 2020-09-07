## Climate action

Get the **Climate Panda** sprite to explain the United Nations' Sustainable Development Goal, [Climate action](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-13-climate-action.html) with a specfic action, sound and setting.

Here is the code you have already. There is some music and some text explaining the Climate action goal as well as a script that gets the **Climate Panda** sprite to `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

![climate action starter code](images/climateaction_startercode.png)

Get the **Climate Panda** sprite to respond to the **Main Panda** sprite's `broadcast`{:class="block3events"} which you set up in the previous step (Step 2).

--- task ---

Start a new script with the `when backdrop switches to Climate action`{:class="block3events"} block and use a `show`{:class="block3looks"} block to show the **Climate Panda** sprite on the stage.

![image of the Climate Panda sprite](images/climatepanda-sprite.png)

```blocks3
when backdrop switches to [Climate action v]
show
```

--- /task ---

--- task ---

<<<<<<< HEAD
Set the size of the **Climate Panda**.

![image of the Climate Panda sprite](images/climatenpanda-sprite.png)
=======
Set the size of the **Climate action Panda** sprite:

![image of the Climate action Panda sprite](images/climateactionpanda-sprite.png)
>>>>>>> b7adb551cadd6727f27adcab0f0e2158bc7545d3

```blocks3
when backdrop switches to (Climate action v)
+ set size to (50) %
show
```

--- /task ---

<<<<<<< HEAD
In the starter code, you can see a `wait 5 seconds`{:class="block3control"} and that means that the **Climate Panda** waits for 5 seconds while the **Main Panda** introduces them.

--- task ---

Get the **Climate Panda** to wait 5 seconds before moving as well.

![image of the Climate Panda sprite](images/climatepanda-sprite.png)
=======
In the starter code, you can see a `wait 5 seconds`{:class="block3control"} and that means that the **Climate action Panda** sprite waits for 5 seconds while the **Main Panda** sprite introduces them.

--- task ---

Get the **Climate action Panda** sprite to wait 5 seconds before moving as well:

![image of the Climate action Panda sprite](images/climateactionpanda-sprite.png)
>>>>>>> b7adb551cadd6727f27adcab0f0e2158bc7545d3

```blocks3
when backdrop switches to (Climate action v)
set size to (50) %
show
+ wait (5) seconds
```
--- /task ---

--- task ---

<<<<<<< HEAD
Add blocks so that after `waiting 5 seconds`{:class="block3control"}, the **Climate Panda** gets bigger and smaller.

![image of the Climate Panda sprite](images/climatenpanda-sprite.png)
=======
Add blocks so that after `waiting 5 seconds`{:class="block3control"}, the **Climate action Panda** sprite gets bigger and smaller:

![image of the Climate action Panda sprite](images/climateactionpanda-sprite.png)
>>>>>>> b7adb551cadd6727f27adcab0f0e2158bc7545d3

```blocks3
when backdrop switches to (Climate action v)
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

<<<<<<< HEAD
Get the **Climate Panda** to respond to the next `broadcast`{:class="block3events"} from the **Main Panda** and `hide`{:class="block3looks"} when it is finished explaining its goal.
=======
Get the **Climate action Panda** sprite to respond to the next `broadcast`{:class="block3events"} from the **Main Panda** sprite and `hide`{:class="block3looks"} when it is finished explaining its goal.
>>>>>>> b7adb551cadd6727f27adcab0f0e2158bc7545d3

--- task ---

Start a new script with the `when I recieve next`{:class="block3events"} and `hide`{:class="block3looks"} blocks:

<<<<<<< HEAD
![image of the Climate Panda sprite](images/climatepanda-sprite.png)
=======
![image of the Climate action Panda sprite](images/climateactionpanda-sprite.png)
>>>>>>> b7adb551cadd6727f27adcab0f0e2158bc7545d3

```blocks3
when I receive [next v]
hide
```

--- /task ---

--- save ---
