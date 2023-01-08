# Steer Bot

## Installation

```bash


# Clone the repo
cd <catkin_ws>/src
git clone https://github.com/nguyenphucvinh15/Car-like_Robot.git


# Clone the repo
git clone https://github.com/nguyenphucvinh15/Car-like_drive_controller.git

cd Car-like_Robot

# Build
cd <catkin_ws>
catkin_make
source devel/setup.bash
```

## Run

Start the Gazebo simulation:

```
roslaunch steer_bot_gazebo steer_bot_sim.launch
```

Start Navigation:

```
roslaunch steer_bot_gazebo teb_local_planner.launch
```
