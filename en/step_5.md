## Responsible consumption and development

Get the **Reuse Panda** sprite to respond to the United Nations' Sustainable Development Goal, [Responsible consumption and production](https://www.undp.org/content/undp/en/home/sustainable-development-goals/goal-12-responsible-consumption-and-production.html) with a specfic action, sound and setting.

Just like in the last step, there is some code here with some music and some text explaining the Responsible consumption and production goal as well as a script that gets the **Reuse Panda** sprite to `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

Get the **Reuse Panda** sprite to respond to the **Main Panda** sprite's `broadcast`{:class="block3events"}.

--- task ---

Start a new script with the `when backdrop switches to Responsible comsumption and production`{:class="block3events"} block and use a `show`{:class="block3looks"} block to show the **Reuse Panda** sprite on the stage.

![image of the Reuse Panda sprite](images/reusepanda-sprite.png)

```blocks3
when backdrop switches to [Responsible consumption and production v]
show
```

--- /task ---

--- task ---

Get the **Reuse Panda** sprite to wait 5 seconds for the **Main Panda** sprite's introduction before moving.

![image of the Reuse Panda sprite](images/reusepanda-sprite.png)

```blocks3
when backdrop switches to (Responsible consumption and production v)
show
+ wait (5) seconds
```
--- /task ---

--- task ---

(((((Add blocks so that after `waiting 5 seconds`{:class="block3control"}, the **Energy Panda** sprite moves from side to side.

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
```)))))

--- /task ---

Get the **Energy Panda** sprite to respond to the next `broadcast`{:class="block3events"} from the **Main Panda** sprite and `hide`{:class="block3looks"} when it is finished explaining its goal.

--- task ---

Start a new script with the `when I receive next`{:class="block3events"} and `hide`{:class="block3looks"} blocks.

![image of the Energy Panda sprite](images/climateactionpanda-sprite.png)

```blocks3
when I receive [next v]
hide
```

--- /task ---

--- save ---
