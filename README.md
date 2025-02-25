# Map My World - RTAB-Map SLAM Project

## Overview
This project involves creating a 2D occupancy grid and a 3D OctoMap of a simulated environment using a custom robot with the RTAB-Map package in ROS. RTAB-Map (Real-Time Appearance-Based Mapping) is a widely used SLAM (Simultaneous Localization and Mapping) solution that enables real-time environment mapping and localization.

## Project Goals
- Develop a ROS package to interface with `rtabmap_ros`.
- Modify an existing localization project to integrate an RGB-D camera for SLAM.
- Ensure correct file structure, proper linking, topic mapping, and configuration.
- Generate appropriate launch files for the robot and mapping process.
- Teleoperate the robot to explore the environment and generate a comprehensive map.

## Prerequisites
Ensure that you have the following installed:
- **ROS (Robot Operating System)** - Noetic or Melodic recommended
- **Gazebo** - For simulating the robot environment
- **rtabmap_ros** - ROS wrapper for RTAB-Map
- **Teleoperation package** - To control the robot manually

## Installation & Setup
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/map_my_world.git
   cd map_my_world
   ```
2. Build the workspace:
   ```bash
   catkin_make
   source devel/setup.bash
   ```
3. Install dependencies:
   ```bash
   sudo apt-get install ros-noetic-rtabmap-ros
   ```

## Running the Project
1. **Launch the world and robot:**
   ```bash
   roslaunch map_my_world world.launch
   ```
2. **Start RTAB-Map SLAM:**
   ```bash
   roslaunch map_my_world mapping.launch
   ```
3. **Teleoperate the robot:**
   ```bash
   rosrun teleop_twist_keyboard teleop_twist_keyboard.py
   ```
4. **View the map:**
   ```bash
   rosrun rviz rviz
   ```
   - Add the `Map` and `PointCloud2` topics to visualize the mapping progress.


## Expected Outcome
By teleoperating the robot, you will create a 2D occupancy grid and a 3D OctoMap of the environment, which can be visualized in **RViz**. The robot should be able to map the surroundings accurately, leveraging the RTAB-Map package.

## References
- [RTAB-Map ROS Wiki](http://wiki.ros.org/rtabmap_ros)
- [ROS Tutorials](http://wiki.ros.org/ROS/Tutorials)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

