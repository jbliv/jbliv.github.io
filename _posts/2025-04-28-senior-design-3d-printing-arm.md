---
title: 3D Printing 6-DOF Robot Arm 
layout: post
post-image: /assets/images/me266k/ur5simCover.png
description: A software package for planar slicing, motion planning, and an intuitive UI for slicing and printing using a 6-DOF UR5e robot arm. This project was completed in fulfillment of the requirements for ME 266K and ME 266P.
tags:
- ROS2
- C++
- Python
- Motion Planning
- Software Architecture
---
# Summary

[Github Repo](https://github.com/jbliv/UR_Slicer)

**Problem Statement:** Create a system for slicing and printing of an STL utilizing a UR5e robot arm and integrate a previously designed custom FDM end-effector.

**Project Details:** This project was a senior design capstone project completed during the Spring 2025 semester sponsored by the SiDi Lab at The University of Texas at Austin. This project was a sub-project of a larger goal within the laboratory to create a cooperative manufacturing system with multiple manufacturing agents. The main deliverables for our team are listed below.

* Implement a planar slicing algorithm
* Motion plan for the sliced printing paths
* Create an easy to understand user interface
* Integrate the previously designed end-effector into our software control system

This page will primarily cover my contributions to the project including the overarching software architecture within ROS2, motion planning, and software testing. For details on other aspects of the project please reach out to me by email.

---
# Software Architecture

This project was based in ROS2 using a mix of both Python and C++. I decided to use ROS2 for the project to allow the use of commonly used robotics packages such as MoveIt2 and RViz2. The primary node for the system acted as an action server for the user interface. Slicing and printing requests from the user would come in to the action server, and it would then communicate with the other nodes to complete the printing process. The control of the end effector was managed within a separate node that acted as a service for the main control node to use as a client. The slicing path generator acted as an action server to feed printing paths to the main control node throughout the printing process. The final node was a MoveIt move group that managed the Cartesian motion planning and execution.

*Software Flowchart*

<img src="/assets/images/me266k/software_architecture.png" width="600" height="300" style="max-width: 100%; height: auto;" alt="Software Architecture">

---
# Motion Planning Environment

The motion planning for this project utilizes MoveIt2 to perform Cartesian motion paths along the desired printing trajectory. To account for the custom end effector used, I created a URDF of our modified UR5e arm setup. This was in turn used to create a custom UR control package and a custom MoveIt configuration. 

*Custom URDF*

<img src="/assets/images/me266k/urdf.png" width="400" height="300" style="max-width: 100%; height: auto;" alt="URDF">

---
# Testing in Simulation

Due to the cost and limited access to the robotic components used in this project it was important to have a method of testing in simulation to validate both the planned trajectories and collision avoidance of the arm. To accomplish this I used RViz2 and the MoveIt package to simulate the motion paths of the robot arm along each layer. This was integrated within the user interface for the printing process and required the operator to validate each simulated trajectory before the robot would perform the desired motion.

*RViz Simulation*

<img src="/assets/images/me266k/sim_test.gif" width="600" height="400" style="max-width: 100%; height: auto;" alt="URDF">

---
# User Interface

The user interface featured two primary aspects. The first being a standard IO interface in the bottom corner which is a custom RViz panel and uses QT widgets to create the desired features and buttons. The second major feature of the UI is the interactive marker representing the desired print object. This allows the user to place the object on the bed in the desired print location and orientation. 

*Interactive STL Marker*

<img src="/assets/images/me266k/moving_stl.gif" width="500" height="300" style="max-width: 100%; height: auto;" alt="Moving STL">

*User Interface*

<img src="/assets/images/me266k/user_interface.png" width="1000" height="300" style="max-width: 100%; height: auto;" alt="User Interface">

---
# Results

While this project was not finished during my time working on it which was limited to a single semester, a solid foundation for continued work was created. At the end of my contributions I also created detailed documentation and tutorials for future usage and development to assist those who may not be as familiar with ROS2 in using the package.

---

# Additional Information

[Final Presentation Slides](/assets/KFinalReport.pdf)

For information regarding this project, usage of the code, or questions, please reach out to me by email.