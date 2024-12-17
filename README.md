# Code Documentation for Element 5

## Development
Element 5 was developed using the foundational template of Element 4, which contained a scene transition mechanic and user interface elements. This was then altered to create the idea of a sandbox-type environment, which would include interactive objects in an expansive player space compared to that demonstrated in Element 3 and 4.

### Main Menu

For the user interface of Element 5, several aspects of the template were changed. The colour of the user interface buttons were changed to blue to contrast with the background of the menu. The background image, which uses a skybox, was also changed.


### Game Scene

The ground was expanded in the ```gameScene.ts``` file across its axes, quadrupling it in size. The ground layer was changed to ```floor.png``` with its subdivisions altered, to ensure that the textures were not warped over the surface area.

### Textures

| Scene       | Texture     |
| ----------- | ----------- |
| ```menuScene```   | ```country.env```|
| ```gameScene```   | ```floor.png```, ```crate.png```|

## Player Movement and Implementation of Havok Physics

### Character Movement

Within ```createRunScene.ts```, the player's animations (e.g., walking and idle) are added to the character's skeleton. Key presses (W, A, S, D, arrow keys) control the player's movement, updating position and rotation. The player's animation is toggled between walking and idle states based on directional movement.

### Collision Detection

Within the source file of ```collisionDeclaration.ts```, Havok physics are integrated into the scene for handling collision detection and physics simulation. The collisionDeclaration function sets up a collision callback to log details about collisions. Physics aggregates are created for the ground and game objects. Collision detection is enabled for these aggregates, enabling realistic object interactions and movement.