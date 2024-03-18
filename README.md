# Love2d Template

## Utilize Helper Libraries:

Love2D has a vibrant community with awesome libraries. Here are a few good ones:

- bump.lua: Collision detection
- hump.gamestate: Advanced state management
- anim8: Animation helper
- Tiled: For loading maps created with the Tiled map editor (https://www.mapeditor.org/)

# Cheat Sheet

## Core Functions

### love.load()

- Called once at game start for initialization.
- Use it to load images, sounds, fonts, etc.

### love.update(dt)

- Handles game logic updates.
- dt: Delta time (time since the last frame), use this for smooth movement independent of framerate.

### love.draw()

- Where you draw graphics to the screen.

## Graphics

### love.graphics.newImage("path/to/image.png")

- Loads an image file.

### love.graphics.draw(image, x, y)

- Draws an image at coordinates (x, y).

### love.graphics.draw(image, x, y, rotation, scaleX, scaleY, originX, originY)

- Advanced drawing: adds rotation, scaling, and sets the origin (point of rotation/scaling).

### love.graphics.setColor(r, g, b, a)

- Sets drawing color (0-255 values for red, green, blue, alpha/transparency).

### love.graphics.rectangle("line" / "fill", x, y, width, height)

- Draws a rectangle ('line' for outline, 'fill' for filled).

### love.graphics.setFont(font)

- Sets the font for text drawing.

### love.graphics.print("Text", x, y)

- Draws text on the screen.

## Input

### love.keyboard.isDown("key")

- Checks if a key is pressed ('key' can be "a", "up", "space", etc.).

### love.mouse.isDown(1 / 2 / 3)

- Checks if mouse buttons are pressed (1 for left, 2 for right, etc.).

### love.mouse.getX(), love.mouse.getY()

- Gets the current mouse coordinates.

## Audio

### love.audio.newSource("path/to/sound.wav")

- Loads a sound file.

### source:play()

- Plays the sound source.

### source:stop()

- Stops the sound source.

## Timers

### love.timer.getTime()

- Gets the current time in seconds since the game started.

### love.timer.sleep(seconds)

- Pauses execution for the specified number of seconds.

## Physics (Box2D basics - requires additional setup)

### world = love.physics.newWorld(gravityX, gravityY)

- Creates a physics world with gravity.

### body = love.physics.newBody(world, x, y, "dynamic" / "static" / "kinematic")

- Creates a physical body in the world (types affect how it reacts to forces).

### shape = love.physics.newRectangleShape(width, height)

- Creates a rectangular shape for a body.

### fixture = love.physics.newFixture(body, shape)

- Attaches a shape to a body, giving it a collision form.

## Additional Resources

- Official LÖVE Wiki: https://love2d.org/wiki/love
- LÖVE Cheat Sheet (1.0): https://love2d.org/forums/viewtopic.php?t=2829
- Other Cheat Sheets: You can often find more specialized cheat sheets online covering topics like file I/O, math functions, etc.
