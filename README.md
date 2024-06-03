![image](https://github.com/rohan-bhautoo/StackBot/assets/47154593/40f885a2-4338-4d29-83d2-3d97b93f3b09)

# Stack-Bot
Stack Bot is a small engaging and dynamic game developed using Unreal Engine 5.

### Game Mechanics
- Bot Control: Take command of a bot with simple and intuitive controls. By left-clicking with the mouse, you can guide the bot to follow your cursor's direction seamlessly.
- Orb Generation: Press the space bar to spawn a glowing orb at the bot's location. These orbs play a crucial role in the game's mechanics and interactions.
- AI Bot: The sole mission of AI-controlled bot is to collect all the orbs scattered across the map. Each time an orb is spawned by the player, the AI bot will dynamically adjust its path to retrieve it.

#### Interactive Elements
- Pressure Plates and Doors: When the bot or another object stands on a pressure plate, it triggers the mechanism to open a corresponding door.

![image](https://github.com/rohan-bhautoo/StackBot/assets/47154593/58e9e19f-94a2-49af-9085-58d378dca63a)

### Gameplay Preview
[Gameplay](https://github.com/rohan-bhautoo/StackBot/assets/47154593/74de0956-d820-4ca8-ad53-5bed81207bba)

### Assets
The contents used are from the [Stack'O'Bot project](https://www.unrealengine.com/marketplace/en-US/product/stack-o-bot).

Download Assets Link: [FirstGameInUE5_Source.zip](https://drive.google.com/file/d/1FAVWZ5rLMYez-s6yRl3SwCqREotF4CaG/view?usp=sharing).

In "FirstGameInUE5_Source.zip" you will find:
- Character
    - Animation
      - A_Antbot_Run.fbx
      - A_Antbot_Idle.fbx
      - A_Antbot_Walk.fbx
    - T_Bot_Masks.TGA
    - SKM_Antbot.fbx
    - T_Antbot_Atlas_Eyes.png
    - T_Antbot_Albedo.png
    - T_Antbot_Normal.png
    - T_Antbot_M_R_AO.png
    - T_Antbot_Face_C.png
- Environment
  - Grass
    - SM_GrassClump.FBX
    - T_GrassClump.png
  - Rock
    - RockFlat_01.fbx
    - SM_Boulder.FBX
    - T_RockTileable_BC.TGA
- Landscape
  - T_SandTileabe_BC.tga
  - T_Grass_M.png
- Props
  - SM_Crate.FBX
  - SM_Pickup_Orb.FBX
  - SM_Door.FBX
  - SM_PressurePlate_Platform.FBX
  - SM_PressurePlate_Frame.FBX
  - SM_Modular_WallDoor.FBX
  - T_Plastic_N.tga
  - T_Metal_N.tga
  - T_Metal_R.tga
  - T_Grunge_A.tga
  - T_Ribbing_A.tga
  - T_Ribbing_N.tga

## Player Controller
The player is controlled using the ToogleInput Action Mapping which is set to the Left Mouse Button. Whenever this button is clicked, the player will move to its new location as implemented in BP_PlayerController.

<img src="https://github.com/rohan-bhautoo/StackBot/assets/47154593/0d44aa8b-ba26-456d-b244-52ba4f99fc96" width="100%" alt="PlayerController"/>

#### Action
<img src="https://github.com/rohan-bhautoo/StackBot/assets/47154593/729d257c-7916-4beb-8503-d43d5b568481" width="100%" alt="PlayerController_Action"/>

#### Blueprint
![PlayerController_Blueprint](https://github.com/rohan-bhautoo/StackBot/assets/47154593/25e1342e-7ce0-425f-9a7c-81a5ae7fffbe)

## Interactive Component
Whenever an object collides with the pressure plate, the plates will move in the Z-axis to replicate the action of it being pressed. Once the pressure plate is pressed, the door will open.

<img src="https://github.com/rohan-bhautoo/StackBot/assets/47154593/ccdc2534-4f15-4811-b596-d6ee92d91223" width="100%" alt="Interactive Component"/>

#### Blueprints
<img src="https://github.com/rohan-bhautoo/StackBot/assets/47154593/6cb42333-052e-468a-8888-9dfe4efc44cc" width="100%" alt="Interactive Component Blueprint 1"/>

![Interactive Component Blueprint 2](https://github.com/rohan-bhautoo/StackBot/assets/47154593/4ebdfeba-3e23-4ea0-a6dc-ab92103f3909)

![Interactive Component Blueprint 3](https://github.com/rohan-bhautoo/StackBot/assets/47154593/3290bafb-1ae1-4f51-b3d4-90c1f10575d8)

## AI Controller
The role of the AI Controller is to move the AI Bot to the index 0 of the Orb. If it is found, the FindOrb() function will execute to return the orb object. Every 3 secs, the Move() event of the AI Bot will execute to check if any orbs exist.

<img src="https://github.com/rohan-bhautoo/StackBot/assets/47154593/6eaa58ab-bf7a-4f31-869a-f9960325a688" width="100%" alt="AI Controller"/>

#### Blueprints
![AI Controller Blueprint 1](https://github.com/rohan-bhautoo/StackBot/assets/47154593/c27db45f-2d39-48e4-b6e6-17e238f6f90f)

![AI Controller Blueprint 2](https://github.com/rohan-bhautoo/StackBot/assets/47154593/130ac72a-a526-4ab5-89c3-208f87be691f)

## Spawn Orbs
Orbs are spawned when the player presses space-bar on the keyboard. The orb will be spawn at the player's current location and the AI Bot will advance to collect it.

<img src="https://github.com/rohan-bhautoo/StackBot/assets/47154593/097c37a3-d28f-4f4c-9d54-5b8543cbd354" width="100%" alt="Spawn Orbs"/>

#### Action
<img src="https://github.com/rohan-bhautoo/StackBot/assets/47154593/32461b34-243f-4714-b59a-5385c000f702" width="100%" alt="Spawn Orbs Action"/>

#### Blueprint
![Spawn Orbs Blueprint](https://github.com/rohan-bhautoo/StackBot/assets/47154593/a21d3d5a-f135-4a44-891e-d763d8e5a06a)

## Effects
Effects are used to enhance the game experience and bring the game world to life. Below is a list of effects that were created directly inside Unreal Engine 5.

### SFX_FootStep
The audio was created with MetaSoundSource which adds a small sound effect to the bot after each step.

![image](https://github.com/rohan-bhautoo/StackBot/assets/47154593/31ae0b0f-1adc-43bc-88c5-79b79ef8d626)

### FX_Dust
Footstep dust particles were created with Niagara system, adding visual flair and a sense of movement to the bot.

<img src="https://github.com/rohan-bhautoo/StackBot/assets/47154593/549a7e49-c7cd-4f08-a44e-0a771e3bb520" width="100%" alt="FX_Dust"/>

### Camera Shake
After each interation with the pressure plate, the camera will shake, enabling the player to know that the door has been opened.

<img src="https://github.com/rohan-bhautoo/StackBot/assets/47154593/1413f144-438b-473a-b597-4c57ade14239" width="100%" alt="Camera Shake"/>
