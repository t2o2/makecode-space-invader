
### Space Invaders with MakeCode Arcade: A Tutorial for Kids

**Objective**: In our game, you'll be the pilot of a spaceship trying to defend Earth from waves of alien invaders. Shoot them down before they reach you!

----------

#### 1. **Setting Up**

-   Go to the [MakeCode Arcade website](https://arcade.makecode.com/).
-   Click on 'New Project'.
-   Give your project a name, like "Space Invaders".

----------

#### 2. **Designing the Background**

-   Click on the `Scene` category.
-   Drag the `set tilemap to tilemap` block to the `on start` loop.
-   Click on the gray tilemap square (the tilemap editor) and add walls like [here](https://github.com/t2o2/makecode-space-invader/blob/main/imgs/wall.png?raw=true) 

----------

#### 3. **Creating the Player's Spaceship**

-   Click on the `Sprites` category.
-   Drag the `set mySprite to sprite of kind Player` block into the `on start` loop.
-   Click on the gray square (the sprite editor). Design your spaceship.
-   Set the spaceship to initial position, go to `Sprites` and drag `set mySprite position to x 80 y 110`
-   To move the spaceship, go to `Controller` and drag `move mySprite with buttons` to the workspace. Set `vx` to 100 and `vy` to 0

[On Start Code](https://github.com/t2o2/makecode-space-invader/blob/main/imgs/on_start.png?raw=true)

----------

#### 4. **Shooting Lasers**

-   In `Sprites`, find the `on button A pressed` block and drag it to the workspace.
-   Inside this block, use the `create projectile from sprite` block. This will make your spaceship shoot a laser when the A button is pressed.
-   Design your laser using the sprite editor.

----------

#### 5. **Creating Alien Invaders**

-   We want the aliens to appear at random positions at the top and move downwards.
-   Use a `game loop` (like `on game update every 1000 ms`) from the `Game` category.
-   Inside the loop, create an alien sprite at a random position on the top edge.
-   Set its velocity to make it move downwards.
-   Design your alien invaders using the sprite editor.

----------

#### 6. **Collisions**

-   We want to destroy the alien when it's hit by a laser and also destroy the laser.
-   Use the `on sprite of kind overlaps other sprite of kind` block from `Sprites`.
-   Set it to detect overlap between a projectile (laser) and an alien.
-   Inside this block, use the `destroy` block to get rid of both the alien and the laser.

----------

#### 7. **Losing the Game**

-   If an alien reaches the bottom, the player should lose.
-   In the same `game loop` where you created the alien, check if the alien's Y position is greater than a certain value (near the bottom).
-   Use the `game over` block from `Game` to end the game if an alien gets too close.

----------

#### 8. **Scoring Points**

-   Every time an alien is destroyed by a laser, the player should earn points.
-   After destroying the alien (in the overlap block from step 6), use the `change score by` block from `Info` to add points.

----------

#### 9. **Testing and Tweaking**

-   Click the play button to test your game.
-   Adjust the speeds, frequencies, and other values to make the game more fun and challenging.

----------

#### 10. **Adding Sounds and Effects**

-   MakeCode Arcade offers a variety of sounds and effects.
-   Add a shooting sound when the laser is fired, an explosion sound when an alien is destroyed, and a sad tone when the game is over.

----------

#### 11. **Sharing Your Game**

-   Once you're happy with your game, click on the share button.
-   Get a link to your game and share it with your friends and family.