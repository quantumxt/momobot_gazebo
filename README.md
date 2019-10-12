# MOMOBot Gazebo
![MOMOBot Gazebo](assets/momo_gz_logo.png)

## Pre-requisite
This model is tested on Gazebo 9, so it is assumed that Gazebo simulator is already installed.

## Dependencies
#### Teb local planner
A plugin to the base_local_planner of the 2D navigation stack, install the relevant dependencies via *rosdep*.
```
$ rosdep install teb_local_planner
```

## Installation
### ROS
Git clone the repository & place the directories in your workspace (E.g. catkin_ws).
Compile the workspace via *catkin_make* and the packages are ready to use!
```
$ catkin_make
```
> **Note**: Please install the required depnedencies before compilation.
### Gazebo
Copy all the models from the *mo2bot_gazebo/models* directory into the *.gazebo/models* directory. (Should be located in the */home/{user}/* directory.)
```
cp -r mo2bot_gazebo/models/* ~/.gazebo/models
```

## Usage
### Launching Gazebo World
![MOMOBot in compound world](assets/cpd_world.png)
Launches Gazebo simulator with the robot model in the Compound World:
```
$ roslaunch mo2bot_gazebo mo2bot_world.launch
```

### Navigation
Navigation with teb_local_planner plugin:
```
$ roslaunch mo2bot_control nav.launch
```
