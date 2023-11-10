
# Webots-EchoSphereRobot

![My Project Image](/images/myimage.png)

## Project Overview
This repository contains the code for an autonomous robot designed to navigate through its environment, search for a specific ball using neural network, and respond to voice commands for additional functionalities like controlling lights. The robot is equipped with obstacle avoidance capabilities, making it adept for indoor navigation.

## Key Features
- **Ball Detection**: Implements neural network techniques to detect a specific ball.
- **Voice Commands**: Interprets and responds to specific voice commands.
- **Obstacle Avoidance**: Uses distance sensors to navigate around obstacles.
- **Light Control**: Ability to control lights via voice commands.

## Technologies and Libraries
- **Language**: Python
- **Extracting image from camera**: OpenCV `cv2` module
- **Speech Recognition**: Google `speech_recognition` module
- **Neural Network**: Roboflow `roboflow` module
- **Simulation Environment**: Webots
- **Supervisor API**: Webots Supervisor API for controlling light
- **Numpy**: `numpy` module

## Functions

### `find(object)`
- Description: Attempts to find an object (in this case, a ball) using the robot's camera.
- Parameters: `object` (str) - The object to be found.
- Returns: Boolean - `True` if the object is found, `False` otherwise.

### `voice_command(command)`
- Description: Executes actions based on the received voice command.
- Parameters: `command` (str) - The voice command to be processed.
- Supported Commands: 
  - `"start"`: Initiates the ball search.
  - `"find"`: Activates ball finding mode.
  - `"hey robot turn on the light"`: Turns on the light.
  - `"hey robot find the ball"`: Run `SEARCHING` mode and function `find`.

### `change_color(start_color, end_color, duration)`
- Description: Changes the color of the robot's light over a specified duration.
- Parameters: 
  - `start_color` (list): Initial color in RGB.
  - `end_color` (list): Final color in RGB.
  - `duration` (int): Time in seconds over which the color change occurs.

### `network:()`
- Description: Apply `soccer-balls-caltech-256` Roboflow API
- Parameters: 
	- None. We take image from `drive_controller.py` file using `cv2` module. 

## Installation
Download .zip file from repository and unpack it. After this open Webots.

## Usage
Run simulation. If you want to change your voice commands you can create new and define them in `voice_command` function from `drive_controller.py` file. Library `sr` need internet connection.
