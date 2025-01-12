[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MjLLqDcN)
# HW1
## W1L2 In-Class Activity

Put your notes from the W1L2 (Thurs, Jan 9) in-class activity here.
HW1 activity

1. Objects：
UI：
    1） seeds planted UI
    2） seeds remaining UI
Players
Plants

2. Attributes and Actions:
Attributes:
    -Bunny sprite
    -Seed sprite
Actions:
    -Movement: 
        -input  -WASD
        -output -player changing locations
    -Planting seeds:
        -input -press space
        -output -if player has seeds remaining: 1 seed is planted at player’s location：     
            decreases seed count + increases plant count
     
3. How do these objects act on and affect each other:
        Player plants one seed by hitting the space, by doing this, the seeds planted UI will be added one and seeds remaining UI will be minused one. This will be repeated until the seeds run out.


## Devlog
Prompt: Include the HW1 break-down exercise you wrote during the Week 1 - Lecture 2 (Jan 9) in-class activity (above). If you did not attend and perform this activity, review the lecture slides and write your own plan for how you believe HW1 should be built. If your initially proposed plan turned out significantly different than the activity answers given by Prof Reid, you may want to note what was different. Then, write about how the plan you wrote in the break-down connects to the code you wrote. Cite specific class names and method names in the code and GameObjects in your Unity Scene.


Write your Devlog here!
This assignment is much easier than last quarter's final project. It helps me to review the knowledge I learned in GDIM 31. 

In-class activity helps me a lot. At first, I don't know the difference between attributes and actions. Thus I wrote the movements in attributes and wrote how to code in actions. After Prof Reid gave the answer, I knew that sprite or other features of the object are attributes. Movement and planting are actions. 

The plan I wrote in breakdown connects well to my implementation. It listed what I need to achieve clearly. With by listing every "if", I can code logically. The primary differences were in how specific attributes and actions were detailed and how to hook them together. The UI confused me at beginning, because I didn't know whether to hook the script with text or num. What's more, I hooked player's script plant count UI with UI script instead of the canvas. These mistakes messed up my working. It took me a lot of time to check the wrong hooks. With my classmate's help, I figured out the plant count UI is a component, not a script.

Player Movement:
    Class: Player : MonoBehaviour
    Method: Update() 
    
Planting Seeds:
    Class: Player : MonoBehaviour
    Method: PlantSeed() 

Plant count UI:
    Class: PlantCountUI : MonoBehaviour
    Method: UpdateSeeds ()

GameObjects：
    Player:
        Player script, 
        SpriteRenderer for the bunny sprite, and a Rigidbody2D for movement.
    UI Elements:
        Seeds Planted UI
        Seeds Remaining UI
    Plant Prefab

## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites
-