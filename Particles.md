# Unity Particle Systems
 ### In short PS in unity have different modules that controls different aspects of the system.
 
 ## Enable To Use Modules
  - Main Module
    ``` bash
		Loop - Duration Of The System - Player Automatically
	    Start Lifetime - How Long it should last 
		Start Speed - Velocity of the particle
		Color - Self Explainatory
		Gravity - Gravity of Particle
		Simulation Space - Follow Or Move Independent
	```
	
	```bash
		Modifiers 
		---------
		Different for each properties like - Random between two variables;
	```	
  - Emission -> Handles The Creation Of Particles
	```bash
		Rate over Time - How much time passes before emission.
		Rate over distance - how far the object has to move to emit another particle.
		Burts - At Once 
	```
  - Shape
	```bash
	Shape - Shape Of The Emitter
	Rest is just self explanatory
	```
  - Renderer -> Look of particles
	```bash
		Render Mode - 2d or 3d mesh etc
	```
 > Over Lifetime Modules -> After Emission Properties
	
	- Speed 
	
			Over Time & Rate Over Time
	
	- Noise 
			Strength - Is how much influence
			Freq  - Smoothness
			ScrollSpeed - Change noise applied over time 
			Octaves - How many Layers we stack on each other
			
	- Collision
	
			Using Type as Plane -> Optimization , Bounce Factor & Damp
		
	- SubEmitter ( Water Droplet -> Ripple )
	
			Create particles from particles
			
	-Texture Sheet Animation
	
			Specify texture sheet on grid or number of sprites
			
	- Lights
		
			Fire & Lightning
			Combo of particle & Light 
		
	- Trails 
		
			Trails , use custom trail mat
		
	- Triggers 
	
		Trigger game logic - use docs
		
	- External Forces
	
		Particles affected by Wind etc 
