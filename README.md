# Gazebo Simulation Drone Assets — KRTI 2025

This repository contains the drone model and simulation assets developed by the BINUS ASO AeroBASE team for the **Kontes Robot Terbang Indonesia (KRTI) 2025**.

## 🛩️ Overview

The drone is modeled for integration with **Gazebo Sim** and **ROS 2 Jazzy**, supporting both visual and physics-based simulation for autonomous flight tasks. This repository includes:

- ✅ Full SDF/URDF drone model
- ✅ Meshes for frame, propellers, and camera mounts
- ✅ Sensor configurations (camera, IMU, LiDAR-ready) **NOT IMPLEMENTED**
- ✅ Coordinate transform trees (`tf`) **NOT IMPLEMENTED**
- ✅ Launch files for testing in simulation

## 📁 Folder Structure


```plaintext
drone_model/
├── drone_model/         # Workspace or subproject directory
├── install/             # Colcon installation directory (build output)
├── log/                 # Colcon log directory
├── materials/           # Gazebo material scripts/textures
├── meshes/              # STL or DAE 3D models for the drone
├── src/                 # ROS 2 source packages
├── urdf/                # URDF files for drone structure
├── drone.urdf           # Top-level drone URDF file
├── LICENSE              # License file (e.g., MIT)
├── model.config         # Gazebo model configuration file
├── model.sdf            # SDF file for Gazebo integration
└── README.md            # Project documentation
```


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
```
Launch the Drone in Gazebo
```
ros2 launch drone_description bringup.launch.py
```
You can also spawn the drone in custom environments via:
```
ros2 launch drone_description spawn_drone.launch.py world:=your_custom_world
```


## 📷 Sensors Included **NOT IMPLEMENTED YET**

| Sensor         | Type      | Interface     |
|----------------|-----------|---------------|
| IMU            | Simulated | `/imu`        |
| Camera (Front) | RGB       | `/image_raw`  |
| LiDAR (Optional)| 2D/3D     | `/scan`       |

---

## 🛠️ Development Team

- **Gareth** – [github.com/theonegareth](https://github.com/theonegareth)

BINUS ASO School of Engineering  
**AeroBASE – Research & Development Division**  

📍 BINUS University  
✉️ Contact: aerobase.team@gmail.com

---

## 📄 License

**MIT License**  
Feel free to use or modify this project for educational or non-commercial KRTI-related work.

