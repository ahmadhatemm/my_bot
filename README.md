# ROS 2 Humble and Gazebo Simulation

This repository contains the technical implementation for simulation task. It features a general-purpose robot model developed in ROS 2 Humble and Gazebo to demonstrate core robotics tasks, sensor integration, and environmental interaction[cite: 2].

### Project Structure
The files are organized as follows based on the simulation requirements[cite: 2]:

* **description**: Contains the robot's URDF and Xacro files, defining the physical structure and visual components[cite: 1, 2].
* **config**: Sensor and controller configurations for the drive system and data streams[cite: 1, 2].
* **launch**: Launch scripts to initialize the robot state and spawn the model into the Gazebo world[cite: 1, 2].
* **worlds**: The custom Gazebo environment featuring the ArUco marker poles required for perception testing[cite: 2].
* **CMakeLists.txt and package.xml**: Build system files for the ROS 2 workspace[cite: 1, 2].

### Robot Features
* **Movement**: Uses a differential drive plugin for realistic motion control[cite: 1, 2].
* **Sensors**: Integration of camera and IMU sensors to provide environmental feedback and orientation data[cite: 1, 2].
* **Physics Stability**: Implementation of custom inertia macros to resolve physics anomalies such as robot bouncing, ensuring stable contact with the ground[cite: 1].
* **Visualization**: Added specific material colors to the model to improve visibility and debugging during testing[cite: 1].

### Installation and Setup
To set up this project, first ensure you have a ROS 2 Humble environment running on Ubuntu 22.04[cite: 2]. Create a new ROS 2 workspace folder and a subdirectory named **src**. Inside the **src** directory, use the git clone command followed by the repository link to download the files. Navigate back to the root of your workspace and use the **colcon build** command to compile the package. After the build completes successfully, source the setup file in your install folder so that ROS 2 can find the new package and its launch files[cite: 2].

### How to Run
To start the simulation and spawn the robot into the custom world, run the following command in your terminal:

`ros2 launch articubot_one launch_sim.launch.py`
