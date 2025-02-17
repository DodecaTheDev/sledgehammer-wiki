# Sledgehammer Guidebook
A wiki for how to use Sledge to it's maximum capacity.

# Functions
### These are functions that you can use in text input boxes.

## random(x,y)
#### Generates a random integer between X and Y.
```
random(0,50)
```
##### Would return a random integer between 0 and 50


## abs(x)
#### Outputs a positive value, regardless of the number.
```
abs(-5)
abs(5)
```
##### Both would return 5

## sine(amp, wavelength, time)
#### Outputs a sine_wave height at a certain time
```
sine_wave(25,25,index*50)
```
##### Returns the height of a sine wave with the amplitude of 25 and wavelength of 25 at time index*50

## snap(number, grid_size)
#### Returns a number snapped to a grid value
```
snap_to_grid(random(0,50),25)
```
##### Would return 0, 25, or 50.


# Variables
### These are variables that you can use in text input boxes.

## Group Variables
### i
##### Returns the index of a parented object

### x / xpos
##### Returns the x of a parented object

### y / ypos
##### Returns the x of a parented object

### spawn_amount
##### Returns the amount of instances spawned by a parent

## Camera Variables
### cam_x
##### Returns the x position of the camera

### cam_y
##### Returns the y position of the camera

## Player Variables
### plr_x
##### Returns the x position of a player

### plr_y
##### Returns the y position of a player

### plr_dir
##### Returns the angle towards the nearest player

# Params
### {TEXT} - String input, compatible with Functions and Variables.
### {BOOLEAN} - Binary (True or False).
### {DROPDOWN} - A predetermined set of options.
### {ENEMY} - A spawned enemy with it's params.
### {SPRITE} - An image to be used.
### {COLOR} - A color with a picker.

# Enemies

## Groups

## Enemy Group
###### Spawns a single object many times
### x
#### {TEXT}
##### The x position to spawn at (can be referred to in children using x or xpos) 

##

### y
#### {TEXT}
##### The y position to spawn at (can be referred to in children using y or ypos) 

##

### spawn
#### {ENEMY}
##### The enemy to spawn

##

### spawn amount
#### {TEXT}
##### The amount of the enemy to spawn (can be referred to in children using spawn_amount)

##

### spawn delay
#### {TEXT}
##### The delay between spawning instances



## Parent Group
###### Spawns a pair of objects many times
### x
#### {TEXT}
##### The x position to spawn at (can be referred to in children using x or xpos) 

##

### y
#### {TEXT}
##### The y position to spawn at (can be referred to in children using y or ypos) 

##

### spawn one
#### {ENEMY}
##### The first enemy to spawn

##

### spawn two
#### {ENEMY}
##### The second enemy to spawn

##

### spawn amount
#### {TEXT}
##### The amount of the enemy to spawn (can be referred to in children using spawn_amount)

##

### spawn delay
#### {TEXT}
##### The delay between spawning instances



## Probability Spawn
###### Chooses between two objects to spawn
### x
#### {TEXT}
##### The x position to spawn at (can be referred to in children using x or xpos) 

##

### y
#### {TEXT}
##### The y position to spawn at (can be referred to in children using y or ypos) 

##

### spawn one
#### {ENEMY}
##### The first possible spawn

##

### spawn two
#### {ENEMY}
##### The second possible spawn

##

### probability
#### {TEXT}
##### The chance to spawn



## Sequence
###### Spawns an object in a sequence
### x
#### {TEXT}
##### The x position to spawn at (can be referred to in children using x or xpos) 

##

### y
#### {TEXT}
##### The y position to spawn at (can be referred to in children using y or ypos) 

##

### spawn one
#### {ENEMY}
##### The first enemy to spawn

##

### spawn two
#### {ENEMY}
##### The second enemy to spawn

##

### delay
#### {TEXT}
##### The delay between spawning *this* instance
