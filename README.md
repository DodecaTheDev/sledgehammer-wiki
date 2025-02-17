# Sledgehammer Guidebook
A wiki for how to use Sledge to it's maximum capacity.

# FUNCTIONS
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


# VARIABLES
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
