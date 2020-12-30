### Player Movement

#### Concept

Predetermined by the PlayerController Component ( Supports Controller by default )

- Vertical Movement = 1 , -1
- Horizontal Movement = 1 , -1

local for relativity - faced direction concept

---

### Script
 - Get Input Value
 
     ```bash
        float xAx = Input.GetAxis("Horizontal");
        float zAx = Input.GetAxis("Vertical"); 
     ```
 - use Vector3 variable to store the movement of the player
    ```bash
        if we use Vector3 moveVar = Vector3(xAx , 0f , zAx);
        {
         xAx & zAx are global -> relativity is lost to the player directions 
        }
    ```
  
    ``` So : We use ```
    
    ```bash
        Vector3 move = transform.right * xAx + transform.forward * zAx;
        
        transform.right -> takes the direction the player is facing and moves right
    ```
       
 - Once we've done this much we can simply get the PlayerController component to get the input from the move variable 
 - ``` public CharacterController controller; --> reference to the playerController component of the Main-Player Object ```
 - the controller object has a function called ``` .Move() ``` which takes in a Vector3 input
 - Since we already made a vector3 for move we can simply pass it in with the ``` Move(move) ```; as a parameter and we are good to go.
 
 ### Jumping
 
 - If you have configured ```isGrounded``` & ```gravity```  & ```velocity``` then :
  
   we know : velocityToEscape gravity and gain +ve velocity = sqroot( height x -2 x gravity ) or simply -> to jump high we need to escape the down pull of gravity.
   
  ```bash 
    if (Input.GetButtonDown("Jump") && isGrounded)
        {
            velocity.y = Mathf.Sqrt(JumpHeight * -2f * gravity);
        }
  ```
