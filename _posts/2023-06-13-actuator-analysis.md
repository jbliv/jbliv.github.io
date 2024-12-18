---
title: Novel Bowden Cable Actuator Analysis
layout: post
post-image: /assets/images/bowden-actuator/cover.png
description: An overview of life cycle testing, torque bandwidth, and positional hysteresis performed to analyze a novel bowden cable actuator.
tags:
- Data Analysis
- Design
- Manual Machining
---
# Summary

**Problem Statement:** Create a suite of tests and necessary fixtures to validate the capabilities of a novel bowden actuator designed by a coworker of mine.

**Project Details:** This project was given to me during my robotics engineering internship at [Contoro Robotics](https://www.contoro.com/). Due to the private intellectual property related to this design, no pictures of the actuator will be included.

---
# Tests Created

**Life Cycle Testing:** One of the primary concerns regarding this new actuator was it's lifespan and wear over time. To evaluate this I assisted in setting up the actuator to rotate back and forth under a standard operating load for extended periods of time. To do this I calculated the standard load and attached a weight at a certain distance from the end effector to provide this load.

**Torque Bandwidth:** To analyze the bandwidth of the torque we used a chirp test to send a sinusoidal signal with a decreasing period as shown in the cover picture. The end effector was held static and the force at the end effector was measured using a force gauge and compared to the input sinusoidal signal. This helped evaluate the bandwidth of the end effector. I designed the rig for holding the end effector static and measuring the load. Below are a few images of components I designed and machined on a manual mill. 

*Force Gauge Mount*

<img src="/assets/images/bowden-actuator/forceGauge.jpg" width="400" height="200" style="max-width: 100%; height: auto;" alt="Force Gauge Mounting Plate">

*Actuator Mounting Plate*

<img src="/assets/images/bowden-actuator/actuator.jpg" width="400" height="200" style="max-width: 100%; height: auto;" alt="Actuator Mounting Plate">


**Positional Hysteresis:** Another important metric for this actuator was repeatable positional accuracy. This was analyzed by comparing commanded position to actual position when approaching the commanded position from either side.

---
# Key Takeaways and Skills Utilized

This project provided me with lots of great insights into actuator design and what metrics are important. It also gave me great experience in designing tests to validate components as well as an opportunity to learn more about life cycle testing.

**Skills Used**
* Manual Machining
* Data Analysis
