# ARCADE: Scalable Demonstration Collection and Generation via Augmented Reality for Imitation Learning
This repo is the codebase for the 2024 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS 2024).

# Table of Contents
- [Unity and ROS ARCADE components](#unity-and-ros-arcade-components)
- [Requirements](#requirements)
- [Initial Setup](#initial-setup)
- [ROS Setup](#ros-setup)
  - [Building the Docker container](#building-the-docker-container)
  - [Running the container](#running-the-container)
  - [Reopening the container](#reopening-the-container)
  - [Running relaxed_ik](#running-relaxed_ik)
- [Unity Setup](#unity-setup)
  - [Aligning the virtual robot to the real robot](#aligning-the-virtual-robot-to-the-real-robot)
  - [Viewing with a Hololens via Holographic Remoting](#viewing-with-a-hololens-via-holographic-remoting)
- [Citing](#citing)


# Unity and ROS ARCADE components
This branch contains the Unity and ROS components (i.e., "AR-assisted Demonstration Collection" section in the paper) for the ARCADE project. Download the repository and follow the instructions below to get started.

We'll release the codebase ASAP for the rest sections when it's cleaned up :)

## Requirements
- Windows Machine
- WSL2
- Docker Desktop
- Unity 2020.3.38f1

## Initial Setup
Clone the files in this branch
```
git clone -b Unity_ROS https://github.com/YY-GX/ARCADE.git
```

Move the ROS folder to your WSL2 home directory and keep the Unity folder on your windows machine.

## ROS Setup
The ROS files are run in a Docker container to avoid any dependency issues.

### Building the Docker container
```
make build_ros_arcade
```

### Running the container
```
make run_ros_arcade
```

### Reopening the container
Check the container ID first four digits
```
docker container ls -a
```

Then start the container
```
make start_ros_arcade <First four digits of Container ID>
```

### Running relaxed_ik
Right click on the black area of the Terminator window, then click split horizontally to open up a second window. 

In one window run relaxed_ik
```
roslaunch relaxed_ik_ros1 demo.launch
```

To connect to Unity, in the other window run
```
hostname -I 
```

Take the ip address, in my case it was 172.17.0.2, and input that as the tcp_ip

```
roslaunch ros_tcp_endpoint endpoint.launch tcp_ip:=172.17.0.2 tcp_port:=10000
```

## Unity Setup
Open the Unity project. Within the /Assets/Scenes folder there are two scenes.

1. HandTrackingScene: Tracks the user's hand and sends the data to ROS, the configuration utilized by ARCADE.
2. ManipulateEEByHandScene: Allows the user to manipulate the end effector of the robot by grabbing the robot's hand and moving it around.

Press play look at the QR code to align the scene to the QR. The project should connect to the docker container. If not, then make sure you are using the correct IP address by typing `hostname -I` in the WSL2 terminal and using the correct IP address in the Unity project, within the ROSConnectionPrefab.

Without the Hololens, the space bar can be used to simulate a hand.

### Aligning the virtual robot to the real robot
To align the virtual robot to the real robot, make sure you have set the QR code in a static position relative to the robot. Then, move the MoveThisToAlignRobotWithRealRobot object in the QR/QROrigin object in the hierarchy. Write down the new Position and Rotation values and update the values in the MoveThisToAlignRobotWithRealRobot object in the hierarchy after stopping the game so that the values persist.

If you are having further connection difficulties, you can reference the following videos for help: https://www.youtube.com/watch?v=3KMhdGV6Ql8 and https://www.youtube.com/watch?v=3KMhdGV6Ql8

### Viewing with a Hololens via Holographic Remoting
If you would like to run this on the HoloLens, you can use the Holographic Remoting feature in Unity. To do this, you will need to download the Holographic Remoting Player app on the HoloLens then, using the IP address displayed in the app, update the IP address in the Mixed Reality -> Remoting -> Holographic Remoting for Play Mode tab in the Unity project. Then, enable Holographic remoting and press play.

# Citing
If you find our work useful, please consider citing our [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10801810):
```bibtex
@inproceedings{yang2024arcade,
  title={ARCADE: Scalable Demonstration Collection and Generation via Augmented Reality for Imitation Learning},
  author={Yang, Yue and Ikeda, Bryce and Bertasius, Gedas and Szafir, Daniel},
  booktitle={2024 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
  pages={2855--2861},
  year={2024},
  organization={IEEE}
}
```

