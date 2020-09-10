## Climate action

You are going to get the **Climate Panda** sprite to explain the United Nations' Sustainable Development Goal, [Climate action](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-13-climate-action.html){:target="_blank"}, with a specfic action, sound and setting.

--- task ---

Go to the **Code** tab for the **Climate Panda** sprite.

You will see some code already provided for you. The code includes music and text explaining the Climate action goal as well as a script that gets the **Climate Panda** sprite to `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

![climate action starter code](images/climateaction_startercode.png)

--- /task ---

Get the **Climate Panda** sprite to respond to the `broadcast`{:class="block3events"} in the **Main Panda** sprite. (You set this up in the previous step).

--- task ---

Add a `when backdrop switches to Climate action`{:class="block3events"} block and use a `show`{:class="block3looks"} block to show the **Climate Panda** sprite on the stage:

![image of the Climate Panda sprite](images/climatepanda-sprite.png)

```blocks3
when backdrop switches to [Climate action v]
show
```

--- /task ---

Reduce the size of the **Climate Panda** sprite  so it fits within the scene.

--- task ---

Add a `set size to`{:class="block3looks"} block to `50` percent:

![image of the Climate Panda sprite](images/climatepanda-sprite.png)

```blocks3
when backdrop switches to (Climate action v)
+ set size to (50) %
show
```

--- /task ---

In the starter code, you can see a `wait 5 seconds`{:class="block3control"}. It means that the **Climate Panda** sprite waits for 5 seconds while the **Main Panda** introduces them.

--- task ---

Get the **Climate Panda** sprite to wait 5 seconds before moving:

![image of the Climate Panda sprite](images/climatepanda-sprite.png)

```blocks3
when backdrop switches to (Climate action v)
set size to (50) %
show
+ wait (5) seconds
```

--- /task ---

--- task ---

Add blocks so that after `waiting 5 seconds`{:class="block3control"}, the **Climate Panda** sprite gets bigger and smaller repeatedly:

![image of the Climate Panda sprite](images/climatenpanda-sprite.png)

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

Get the **Climate Panda** sprite to respond to the next `broadcast`{:class="block3events"} from the **Main Panda** sprite and `hide`{:class="block3looks"} when it is finished explaining its goal.

--- task ---

Start a new script with the `when I recieve next`{:class="block3events"} and `hide`{:class="block3looks"} blocks:

![image of the Climate Panda sprite](images/climatepanda-sprite.png)

```blocks3
when I receive [next v]
hide
```

--- /task ---

--- task ---

Now test your program with the new sprite and backdrop.

--- /task ---

--- save ---
