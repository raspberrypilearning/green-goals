## Responsible consumption and development

Get the **Waste Panda** sprite to respond to the United Nations' Sustainable Development Goal, [Responsible consumption and production](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-12-responsible-consumption-and-production.html){:target="_blank"}, with a specfic action, sound and setting.

--- task ---

Got to the **Code tab** for the **Waste Panda**.

You will see some code  already  provided for you. This includes music and text explaining the Responsible consumption and production goal as well as a script that gets the **Waste Panda** sprite to `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

Get the **Waste Panda** sprite to respond to the **Main Panda** sprite's `broadcast`{:class="block3events"}.

--- /task ---

--- task ---

Start a new script with the `when backdrop switches to Responsible comsumption and production`{:class="block3events"} block and use a `show`{:class="block3looks"} block to show the **Waste Panda** sprite on the stage:

![image of the Waste Panda sprite](images/wastepanda-sprite.png)

```blocks3
when backdrop switches to [Responsible consumption and production v]
show
```

--- /task ---

--- task ---

Get the **Waste Panda** sprite to wait 5 seconds for the **Main Panda** sprite's introduction before moving:

![image of the Waste Panda sprite](images/wastepanda-sprite.png)

```blocks3
when backdrop switches to (Responsible consumption and production v)
show
+ wait (5) seconds
```
--- /task ---

To get the **Waste Panda** sprite to move, reuse code from the **Energy Panda** sprite.

--- task ---

Go to the **Code** tab for the **Energy Sprite** and find the repeat loop you used to get the sprite to move. It should look like this:

![image of the Energy Panda sprite](images/energypanda-sprite.png)

```blocks3
when backdrop switches to (Affordable and clean energy v)
point in direction (90)
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

--- task ---

Highlight the repeat loop by clicking on it. Make sure only the 5 blocks you need are highlighted (not the whole script).

--- /task ---

--- task ---

Drag these blocks into the image of the **Waste Panda** sprite and make sure you put them in the script you started earlier in this step:

![image of the Reuse Panda sprite](images/reusepanda-sprite.png)

```blocks3
when backdrop switches to [Responsible consumption and production v]
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

Get the **Waste Panda** sprite to respond to the next `broadcast`{:class="block3events"} from the **Main Panda** sprite and `hide`{:class="block3looks"} when it is finished explaining its goal.

--- task ---

Start a new script with the `when I receive next`{:class="block3events"} and `hide`{:class="block3looks"} blocks:

![image of the Reuse Panda sprite](images/reusepanda-sprite.png)

```blocks3
when I receive [next v]
hide
```

--- /task ---

--- task ---

Now test your program with the new sprite and backdrop.

--- /task ---

--- save ---
