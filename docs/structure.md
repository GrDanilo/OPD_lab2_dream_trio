# Simple 2D Template's structure

# 1. Scenes
* "PlatformerDemo" - scene, where platformer game is
* "TopDownDemo" - scene, where top-down game is
* "TopDownDemo3D" - same top-down game, but 3D
* "URP2DSceneTemplate" - standart empty scene for Universal 2D project
* "SampleScene" - empty scene

# 2. PlatformerDemo scene's objects
* "CharacterPlatformer" (prefab) - player, has "Hand" inside
* "Main Camera" - camera that follows player
* "Managers" - object with PlayerControl.cs
* "TilemapGrid" - grid for the level (contains 3 Tiles)
* "TreeBackground" (prefab) - simple background of trees
* "Grass" (prefabs) - transform object which contains Grass prefabs
* "Lights" - transform object which contains Directional light

# 3. Player's components

* "Sprite Renderer" - common component of 2D sprite
* "Animator" - allows to manage animations
* "Rigidbody 2D" - adds 2D physics to player
* "Capsule Collider 2D" - makes collision hitbox

# 4. Scripts analyse
* "CarryItem.cs" - attaches to carryable objects and defines their properties, such as their offset in the player's hand, throwing behavior, or automatic return to the starting position upon the character's death.
* "CharacterAnim.cs" - manages character animations, automatically switching states (running, jumping, crouching, holding an object) based on player actions.
* "CharacterHoldItem.cs" - governs the character's ability to interact with objects: picking them up, holding them, using them via the action button, or dropping them upon death.
* "CameraFollow.cs" - manages the game camera's behavior, ensuring smooth tracking of the player, restricting movement to the level boundaries, and producing a screen-shake effect when damage is taken.
* "Lever.cs" - handles the operation of level-based levers that the player can activate upon approach to toggle their visual state and send a signal to linked objects (such as doors).
* "ParallaxBackground.cs" - creates a depth (parallax) effect in the level by smoothly shifting the background in response to the main camera's movement.
* "PlayerCharacter.cs" - the core component of the player's physics and logic; it handles health stats and mechanics for acceleration, jumping, and crouching, and also tracks falls outside the level boundaries.
* "PlayerControls.cs" - captures keyboard key presses (movement, jump, action) for a specific player and transmits these commands to the character control system.
* "TheAduio.cs" - acts as a global sound manager that dynamically creates audio channels and plays sound effects in the game without overlapping them.