# Gazebo Simulation Drone Assets — KRTI 2025

This repository contains the drone model and simulation assets developed by the BINUS ASO AeroBASE team for the **Kontes Robot Terbang Indonesia (KRTI) 2025**.

## 🛩️ Overview

The drone is modeled for integration with **Gazebo Sim** and **ROS 2 Jazzy**, supporting both visual and physics-based simulation for autonomous flight tasks. This repository includes:

- ✅ Full SDF/URDF drone model
- ✅ Meshes for frame, propellers, and camera mounts
- ✅ Sensor configurations (camera, IMU, LiDAR-ready)
- ✅ Coordinate transform trees (`tf`)
- ✅ Launch files for testing in simulation

## 📁 Folder Structure

drone_model/ ├── launch/ # ROS 2 launch files ├── meshes/ # STL models for drone components ├── urdf/ or sdf/ # Drone description in URDF or SDF ├── rviz/ # RViz configuration files ├── worlds/ # Gazebo world files for testing ├── config/ # Sensor configs or camera calibration └── README.md


## 🚀 Getting Started

### Requirements

- [ROS 2 Jazzy](https://docs.ros.org/en/jazzy/index.html)
- [Gazebo Sim](https://gazebosim.org/)
- [colcon](https://docs.ros.org/en/rolling/Tutorials/Colcon-Tutorial.html)

### Clone the Repository

```bash
git clone https://github.com/BINUS-ASO-AeroBASE/GZassets.git
cd GZassets

Build the Workspace

cd ~/your_ros2_ws
colcon build
source install/setup.bash

Launch the Drone in Gazebo

ros2 launch drone_description bringup.launch.py

You can also spawn the drone in custom environments via:

ros2 launch drone_description spawn_drone.launch.py world:=your_custom_world

📷 Sensors Included
Sensor	Type	Interface
IMU	Simulated	/imu
Camera (Front)	RGB	/image_raw
LiDAR (Optional)	2D/3D	/scan
🛠️ Development Team

BINUS ASO School of Engineering
AeroBASE Team – KRTI 2025 Division
📍 BINUS University
✉️ Contact: aerobase.team@gmail.com
📄 License

MIT License. Feel free to use or modify for educational or non-commercial KRTI-related work.
