[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MjLLqDcN)
# HW1
## W1L2 In-Class Activity

Put your notes from the W1L2 (Thurs, Jan 9) in-class activity here.
HW1 activity

1. Objects：
    - UI：
        1. seeds planted UI
        2. seeds remaining UI
    - Players
    - Plants

2. Attributes and Actions:
    - Attributes:
        - Bunny sprite
        - Seed sprite
    - Actions:
        - Movement:
            - input: WASD
            - output: player changing locations
    - Planting seeds:
        - input: press space
        - output
            - if player has seeds remaining:
            - 1 seed is planted at player’s location
            - decreases seed count + increases plant count
     
3. How do these objects act on and affect each other:
Player plants one seed by hitting the space, by doing this, the seeds planted UI will be added one and seeds remaining UI will be minused one. This will be repeated until the seeds run out.

## Devlog
This assignment is much easier than last quarter's final project. It helps me to review the knowledge I learned in GDIM 31. 

In-class activity helps me a lot. At first, I don't know the difference between attributes and actions. Thus I wrote the movements in attributes and wrote how to code in actions. After Prof Reid gave the answer, I knew that sprite or other features of the object are attributes. Movement and planting are actions. 

The plan I wrote in breakdown connects well to my implementation. It listed what I need to achieve clearly. With by listing every "if", I can code logically. The primary differences were in how specific attributes and actions were detailed and how to hook them together. The UI confused me at beginning, because I didn't know whether to hook the script with text or num. What's more, I hooked player's script plant count UI with UI script instead of the canvas. These mistakes messed up my working. It took me a lot of time to check the wrong hooks. With my classmate's help, I figured out the plant count UI is a component, not a script.

Player Movement:
- Class: Player : MonoBehaviour
- Method: Update() 
    
Planting Seeds:
- Class: Player : MonoBehaviour
- Method: PlantSeed() 

Plant count UI:
- Class: PlantCountUI : MonoBehaviour
- Method: UpdateSeeds ()

GameObjects：
- Player:
    - Player script, SpriteRenderer for the bunny sprite, and transform
- UI Elements:
    - Seeds Planted UI
    - Seeds Remaining UI
    - Plant Prefab

## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites

## Prof comments
I'm giving you full credit for this Devlog, but for your next one, I would really like you to write out in full sentences the connections between your plan and your code. I see that you made the connection by listing your objects and their corresponding methods, but next time, please write them out to describe the connection in more depth. 

You should also be careful about using technical terms correctly. I wanted to point out one small error:

> With my classmate's help, I figured out the plant count UI is a component, not a script.

The PlantCountUI script is *also* a Component. When you drag a Script that contains a Monobehaviour class from your Assets onto a GameObject, it becomes a Component. However, the difference you pointed out is still important- it sounds like you were trying to drag the Script from the *Assets* window into the Plant Count UI field on the Player Component, when you actually wanted to drag the PlantCountUI from the *Hierarchy* into that field. The difference is that our Assets window contains stuff that's in our project folders/files, but the Hierarchy window contains GameObjects (and their Components) that are actually in our Scene. I think you understand the difference, so I'm not taking points off, but I want to encourage you to make sure to be specific with your wording so that TAs don't take points off in the future. Let me know if that makes sense!

I'm really glad that the in-class activity helped you understand the difference between actions and attributes, and that the break-down helped you write your code! I'm interested to see if you feel like the HW2 break-down was also helpful. :)

Also, please consider formatting your break-down activities with the hyphen '-' symbol as suggested above, and remove the prompts. This will make it a lot easier for me to read. See the [README formatting guide here](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
