### Mouse Look

#### Concept

- Mouse has 2 axes
- X => Rotate Player About Y Axis
- Y => Camera About X Axis Clamped ( No Player Rotation )
 > Clamping : limiting the rotation angle so that it doesnt rotate to a point behind the player
 
 ___
 
 ## FirstPerson

 ### First Person Mouse Look Script
 ---
 
 - Get Mouse Input ( Axis Indepedent => X & Y seperate )
 - Use Input.GetAxis - function to get ("Mouse X") & ("Mouse Y") ```use Time.deltaTime to avoid controls speed jumps ```
 
 ---
 
 > Mouse X 
  - Get PlayerBody Reference call into update 
  - Rotate(Vector3.up * Mouse X) -> about Y-axis times the mouseX axis rotation
  
 ---
 > Mouse Y
  - Get Rotation About X to be stored in a variable => ``` RotationAboutX -= mouseY; ``` 
  this is because 
  
  ```bash
  if RotationAboutX = mouseY {
        It'll snap reset every frame => stuttering dog shit camera
      }
  ```
  - Since variable is local use transform.localRotation to store camera angle (this is to implement Clamping)
  - var transform^ = ``` Quarternion.Euler(RotationAboutX, 0 , 0); ```
      > Quarternion -> Data types ``` Q.Euler Gives your eulerAngles => (x,y,z) ```
      
  - Clamping : ``` RotationAboutX = Mathf.Clamp(RotationAboutX, -90f, 90f); ```
  
 ---
 
 > Cursor Handling 
  - Since the cursor would appear in the scene we need to handle it.
  - Use start() to handle it with : 
   > ``` Cursor.lockState = CursorLockMode.Locked; ```

 ---
 
 
 ## Third Person
 
 ---
 
