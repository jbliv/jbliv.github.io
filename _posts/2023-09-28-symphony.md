---
title: Symphony - One Armed Teleoperation Exoskeleton
layout: post
post-image: /assets/images/symphony/cover.png
description: An overview of my mechanical design contributions towards the Symphony teleoperation exoskeleton. 
tags:
- CAD
- DFM
- GD&T
---
# Summary

**Problem Statement:** Modify the Harmony SHR therapy exoskeleton to create a one-armed teleoperation device with haptic feedback to serve as a controller for a Kuka industrial robot arm.

**Project Details:** This project was given to me during my robotics engineering internship at [Contoro Robotics](https://www.contoro.com/). I owned the stand, stand-top, and control box regions of this redesign. 

---
# Overview of Contributions

**Stand-Top Region:** The stand top region consisted of 3 CNC milled aluminum parts. This region was split into multiple pieces to reduce material and machining costs and included locating features to ensure exact alignment. This region also contained mounting points for multiple switches, wiring, and the arm itself.

*Partial Stand-Top*

<img src="/assets/images/symphony/partTop.jpg" width="480" height="260" style="max-width: 100%; height: auto;" alt="Partial Stand Top">

*Full Stand-Top with Arm Mounted*

<img src="/assets/images/symphony/fullTop.jpg" width="480" height="260" style="max-width: 100%; height: auto;" alt="Full Stand Top">

**Control Box:** The primary motivation behind the control box redesign was to create as compact of a storage solution as possible. My design did precisely that while ensuring proper spacing of power supplies for heat dissipation, cable routing channels, and easy assembly. The design consisted of two main pieces, the first being the internal structure and the second being the external casing. The internal structure utilized welded on DIN rail mounts for a majority of the components and mounting points for the rest such as the PC that ran the robot. The external casing was a single piece that had the gaps welded closed and was coated for a better looking finish. This casing was designed to be incredibly easy to remove.

*Internal Structure*

<img src="/assets/images/symphony/noWire.jpg" width="400" height="200" style="max-width: 100%; height: auto;" alt="Internal Structure">

*Outer Casing*

<img src="/assets/images/symphony/case.jpg" width="400" height="200" style="max-width: 100%; height: auto;" alt="Outer Casing">

*Components Installed*

<img src="/assets/images/symphony/noCase.jpg" width="400" height="200" style="max-width: 100%; height: auto;" alt="All components installed">

*Full Case*

<img src="/assets/images/symphony/fullCase.jpg" width="400" height="200" style="max-width: 100%; height: auto;" alt="All components installed">

**Implementation:** In addition to my design contributions I also set up a toggle switch for controlling the lifting column that the arm was mounted on. This was accomplished by using an H-Bridge to allow a 5V signal to control the much higher voltage of the lifting column.

---
# Key Takeaways and Skills Utilized

During this project I applied my skills in CAD and GD&T to design and create drawings for sheet metal, and CNC milled parts to send to a manufacturer to create. One of my key takeaways was to minimize unnecessary dimensional accuracies on parts in order to reduce manufacturing costs.

**Skills Used**
* Solidworks
* Sheet Metal Design
* DFM
* GD&T
