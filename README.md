Gameplay & Features
The objective of the game is simple: guide the dragon through the gaps between the castle towers without crashing. Each pair of towers you successfully pass earns you a point.

Key Features:
Dynamic Dragon Sprite: The dragon is animated with flapping wings and periodically breathes fire, adding a lively feel to the game.

Adjustable Difficulty: Players can choose from three difficulty levels before starting:

Easy: Wider gaps between towers, slower speed, and lower gravity.

Medium: The standard, balanced experience.

Hard: Narrower gaps, faster game speed, and stronger gravity for a true challenge.

Interactive Controls: The game supports multiple input methods, making it accessible on both desktop and mobile devices.

Keyboard: Press the SPACE bar to flap.

Mouse: Click anywhere on the game screen to flap.

Touch: Tap the screen on mobile devices.

Pause/Resume Functionality: Players can pause the game at any time by pressing ENTER or clicking the pause button (⏸️), and resume when they are ready.

Detailed Graphics: The game features a scrolling background with clouds, a detailed ground with grass, and dynamically generated castle towers with brick textures and fiery tops.

Clean UI: A polished user interface with separate screens for the start menu, game over, and pause states ensures a smooth user experience.

Technologies Used
This project was built from the ground up using fundamental web technologies. No external libraries or frameworks were used.

HTML5: Provides the basic structure of the game, including the <canvas> element for rendering.

CSS3: Used for all styling, including the layout, fonts, button designs, and screen overlays.

JavaScript (ES6): Powers the entire game logic, including:

Rendering graphics on the HTML5 Canvas.

Handling player input and controls.

Implementing game physics (gravity, velocity).

Managing game state (start, running, paused, game over).

Collision detection.

Generating and moving obstacles.
Code Overview
The JavaScript code is self-contained within the <script> tag in the index.html file and is structured logically.

Core Components:
Game State Variables:

gameRunning, gamePaused: Booleans that control the state of the game loop.

score, frames: Keep track of the player's score and the elapsed frames for animation timing.

difficulty: Stores the selected difficulty setting.

Game Objects (dragon, obstacles):

These are JavaScript objects that encapsulate properties (like position, size) and methods (draw(), update()).

The dragon object handles its own physics, including applying gravity, flapping (changing velocity), and rotation based on its movement.

The obstacles object manages an array of tower positions, handles their creation at regular intervals, moves them across the screen, and checks for collisions.

Main Game Loop (loop()):

The loop() function is the heart of the game, powered by requestAnimationFrame() for smooth, efficient animations.

On each frame (if the game is running and not paused), it clears the canvas, updates the positions of the dragon and obstacles, redraws all elements, and increments the frame counter.

Event Listeners:

Event listeners are set up to handle player input from the keyboard (keydown), mouse (click), and touch (touchstart) to trigger the dragon's flap() method.

Listeners for the UI buttons handle starting, restarting, and pausing the game.

Updating the score.

How to Play Locally
