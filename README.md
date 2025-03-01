# Sledgehammer Guidebook
A wiki for how to use Sledge to its maximum capacity.

---

## Functions
### These are functions that you can use in text input boxes.

### `random(x, y)`
Generates a random integer between `x` and `y`.
```sledge
random(0, 50)
```
Would return a random integer between 0 and 50.

---

### `abs(x)`
Outputs a positive value, regardless of the number.
```sledge
abs(-5)
abs(5)
```
Both would return `5`.

---

### `sine(amp, wavelength, time)`
Outputs a sine wave height at a certain time.
```sledge
sine(25, 25, index * 50)
```
Returns the height of a sine wave with an amplitude of 25 and a wavelength of 25 at time `index * 50`.

---

### `snap(number, grid_size)`
Returns a number snapped to a grid value.
```sledge
snap(random(0, 50), 25)
```
Would return `0`, `25`, or `50`.

---

## Variables
### These are variables that you can use in text input boxes.

### Group Variables
- **`i`** - Returns the index of a parented object.
- **`x / xpos`** - Returns the x-coordinate of a parented object.
- **`y / ypos`** - Returns the y-coordinate of a parented object.
- **`spawn_amount`** - Returns the number of instances spawned by a parent.

### Camera Variables
- **`cam_x`** - Returns the x position of the camera.
- **`cam_y`** - Returns the y position of the camera.

### Player Variables
- **`plr_x`** - Returns the x position of the player.
- **`plr_y`** - Returns the y position of the player.
- **`plr_d`** - Returns the angle towards the nearest player.

---

## Param Types
- **`{TEXT}`** - String input, compatible with Functions and Variables.
- **`{BOOLEAN}`** - Binary (True or False).
- **`{DROPDOWN}`** - A predetermined set of options.
- **`{ENEMY}`** - A spawned enemy with its params.
- **`{SPRITE}`** - An image to be used.
- **`{COLOR}`** - A color with a picker.

---

## Default Params
Not to be used with functions or variables.
- **`spawn time`** `{TEXT}` - The spawn time of an enemy.
- **`name`** `{TEXT}` - An internal name to refer to your object as. `default - NONE`

## Common Params
Most attacks have these but some don't
- **`x`** `{TEXT}` - The x position to spawn at (can be referred to in children using `x` or `xpos`). `default - random(0,1920)`
- **`y`** `{TEXT}` - The y position to spawn at (can be referred to in children using `y` or `ypos`). `default - random(0,1080)`
- **`active time`** `{TEXT}` - The time the attack persists. `default - 1500`
- **`warning length`** `{TEXT}` - The time the attack warns the player. `default - 2000`

---
## Enemies

### Bullet
- **`angle`** `{TEXT}` - The direction the bullet points in. `default - 180`
- **`speed`** `{TEXT}` - How fast the bullet moves. `default - 6`
- **`size`** `{TEXT}` - The scale of the bullet. `default - 12`
- **`rotation speed`** `{TEXT}` - How fast the bullet rotates. `default - 12`
- **`sprite`** `{SPRITE}` - The sprite the bullet displays. `default - Square`
- **`apparition time`** `{TEXT}` - How long the apparition lasts. `default - 500`
- **`do sway`** `{BOOLEAN}` - Determines if the bullet shakes in a sine motion. `default - true`
- **`apparition type`** `{DROPDOWN}` - The position of the apparition. `default - over`
```
  over - apparition appears over the bullet.
  under - apparition appears under the bullet.
  none - apparition does not appear.
```

### Beam
- **`size`** `{TEXT}` - The width of the beam. `default - 25`
- **`do punch`** `{BOOLEAN}` - If the beam pushes the camera on impact. `default - true`
- **`do shake`** `{BOOLAEN}` - If the beam shakes on it's axis. `default - false`
- **`direction`** `{DROPDOWN}` - The side of the screen that the beam comes from. `default - any`
```
  left
  right
  up
  down
  any horizontal - left or right
  any vertical - up or down.
  any - up down left or right.
```

### Wall
- **`size`** `{TEXT}` - The width of the wall. `default - 150`
- **`do punch`** `{BOOLEAN}` - If the wall pushes the camera on impact. `default - true`
- **`direction`** `{DROPDOWN}` - The side of the screen that the wall comes from. `default - any`
```
  left
  right
  up
  down
  any horizontal - left or right
  any vertical - up or down.
  any - up down left or right.
```

### Skew Beam
- **`size`** `{TEXT}` - The width of the beam. `default - 25`
- **`height`** `{TEXT}` - The height of the beam. `default - 50`
- **`direction`** `{DROPDOWN}` - Where the beam anchors to. `default - 150`
```
  top
  bottom
```
- **`anchored`** `{BOOLEAN}` - If the beam anchors to the given `direction`. `default - true`

### Bomb
- **`size`** `{TEXT}` - The width of the bomb itself. `default - 50`
- **`instance count`** `{TEXT}` - The amount of bullets the bomb fires.  `default - 12`
- **`instance size`** `{TEXT}` - The scale of the bullets the bomb fires. `default - 12`
- **`flash`** `{BOOLEAN}` - If the screen flashes when the bomb detonates. `default - true`
- **`explosion`** `{BOOLEAN}` - If the bomb creates a small explosion particle upon detonating. `default - false` 
- **`side`** `{DROPDOWN}` - The side of the screen the bomb comes from. `default - any`
```
  left
  right
  up
  down
  any - up down left or right
```
- **`instance speed`** `{TEXT}` - How fast the bullets move. `default - 6`
- **`instance rotation`** `{TEXT}` - How fast the bullets rotate. `default - 6`
- **`instance sprite`** `{SPRITE}` - The sprite the instances display. `default - Square`
- **`apparition type`** `{DROPDOWN}` - The position of the apparition. `default - over`
```
  over - apparition appears over the bullet.
  under - apparition appears under the bullet.
  none - apparition does not appear.
```

---

### Snakes

### Snake
- **`spawn delay`** `{TEXT}` - The time between the instances spawning. `default - 250`
- **`angle`** `{TEXT}` - The rotation the instances move in. `default - random(0,360)`
- **`turn amount`** `{TEXT}` - How much the rotation of the instance path changes. `default - 3`
- **`instance spin`** `{TEXT}` - How much each instance rotates. `default - 5`
- **`size`** `{TEXT}` - The size of each instance. `default - 25`
- **`distance`** `{TEXT}` - The space between each instance. `default - 30`
- **`count`** `{TEXT}` - The amount of instances. `default - 25`
- **`spiral ratio`** `{TEXT}` - A multiplier applied to the `distance` and `size`. `default - 1`
- **`sprite`** `{SPRITE}` - The sprite the instances display. `default - Square`


### Sine Snake
- **`spawn delay`** `{TEXT}` - The time between the instances spawning. `default - 250`
- **`angle`** `{TEXT}` - The rotation the instances move in. `default - random(0,360)`
- **`distance`** `{TEXT}` - The space between each instance. `default - 30`
- **`size`** `{TEXT}` - The size of each instance. `default - 25`
- **`turn amount`** `{TEXT}` - How much the rotation of the instance path changes. `default - 3`
- **`instance spin`** `{TEXT}` - How much each instance rotates. `default - 6`
- **`speed`** `{TEXT}` - How fast the sine wave progresses. `default - 5`
- **`amplitude`** `{TEXT}` - The amplitude of the sine wave. `default - 20`
- **`wavelength`** `{TEXT}` - The wavelength of the sine wave. `default - 20`
- **`count`** `{TEXT}` - The amount of instances. `default - 25`
- **`spiral ratio`** `{TEXT}` - A multiplier applied to the `distance` and `size`. `default - 1`
- **`sprite`** `{SPRITE}` - The sprite the instances display. `default - Square`


### Checker Snake
- **`spawn delay`** `{TEXT}` - The time between the instances spawning. `default - 250`
- **`angle`** `{TEXT}` - The rotation the instances move in. `default - random(0,360)`
- **`size`** `{TEXT}` - The size of each instance. `default - 25`
- **`instance spin`** `{TEXT}` - How much each instance rotates. `default - 5`
- **`count`** `{TEXT}` - The amount of instances. `default - 25`
- **`sprite`** `{SPRITE}` - The sprite the instances display. `default - Square`

---

### Groups

### Enemy Group
Spawns a single object multiple times.

- **`spawn`** `{ENEMY}` - The enemy to spawn. `default - Beam`
- **`spawn amount`** `{TEXT}` - The number of enemies to spawn (can be referred to in children using `spawn_amount`). `default - 5`
- **`spawn delay`** `{TEXT}` - The delay between spawning instances. `default - 50`

### Parent Group
Spawns a pair of objects multiple times.

- **`spawn one`** `{ENEMY}` - The first enemy to spawn. `default - Beam`
- **`spawn two`** `{ENEMY}` - The second enemy to spawn. `default - Bullet`
- **`spawn amount`** `{TEXT}` - The number of enemies to spawn. `default - 5`
- **`spawn delay`** `{TEXT}` - The delay between spawning instances. `default - 50`

### Probability Spawn
Chooses between two objects to spawn.

- **`spawn one`** `{ENEMY}` - The first possible spawn. `default - Beam`
- **`spawn two`** `{ENEMY}` - The second possible spawn. `default - Bullet`
- **`probability`** `{TEXT}` - The chance to spawn. `default - 50`

### Sequence
Spawns an object in a sequence.

- **`spawn one`** `{ENEMY}` - The first enemy to spawn. `default - Beam`
- **`spawn two`** `{ENEMY}` - The second enemy to spawn. `default - Bullet`
- **`delay`** `{TEXT}` - The delay between spawning *this* instance. `default - 500`

