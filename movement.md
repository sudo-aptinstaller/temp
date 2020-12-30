# Movement

### Good controls =>

```bash
- Snappy Movement
- Gravity Consideration ( Physics )
- Proper Jumping Mechanics ( Ground Check )
- Airtime Movement ( Obeys Laws Of Physics or Comical )
- Stepping Up and Down Mechanics
- Slopes Handling and Slidiing
- Doesnt Get Stuck On Objects
```

## Things to consider

 - Gravity
 - Jumping
 - Drag
 - Airtime Movement
 - Slopes
 - Steps
 - Sprinting
 - Crouching
 - Interaction with other physics objects
 
___

# First Person Movement & Controls
## Taken into consideration
 - Character Controller Component
 - RigidBody Component

___

| Character controller | Rigid Body |
| --- | --- |
| Handles Steps | Gravity Built In |
| Handles Slopes | Drag Built In |
| Doesn't get stuck on Walls | Interact With Physics Objects |
| Easy to make Snappy | . . . |

 ### Choice clearly depends on the game that you are making
___

## First Person Indepth Procedure

#### Shortcuts

> Pulling down a camera under a GameObject & Resetting it pushes it inside the player


#### Links

 [Mouse Look Indepth](https://github.com/aptinstaller/unity_minidocs/blob/master/mouselook.md)
 [Keyboard Movement](https://github.com/aptinstaller/unity_minidocs/blob/master/playermovement.md)

### Starting Point

```bash
 - EmptyObject - CharacterControllerComponent - Acts As Collider Also
 - > Child > Graphics
 - Add Mouse Look Script To Empty Object
 ``` 




