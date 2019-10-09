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
If the Willow Garage model could not be loaded or is not found, copy the *willowgarage* directory from the *mo2bot_gazebo/models/* directory to the *.gazebo* directory located in the */home/{user}/* directory.
```
$  cp -r willowgarage/ ~/.gazebo
```


## Usage
### Launching Gazebo World
Launches Gazebo with the robot model in Willow Garage:
```
$ roslaunch mo2bot_gazebo mo2bot_world.launch
```

### Navigation
Navigation with teb_local_planner plugin:
```
$ roslaunch mo2bot_control nav.launch
```
