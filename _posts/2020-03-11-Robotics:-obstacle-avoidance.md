---
layout: post
title:  "Robotics: obstacle avoidance exercise"
description: "My obstacle avoidance proyect in Phyton"
last_modified_at: 2020-02-17
image:
categories: Robotics, Technology
tags: [Robotics, Phyton, cv2, VFF]
---

# 1. Introduction
The objective of this exercise is to complete the entire circuit avoiding the obstacles that the car will find on its trajectory.
For solving this logic problem its required the implementation of an VFF Local Navegation algorithm, wich will be detalled later.

# 2. Hardware
## 2.1. Sensors
The sensor that we have to carry out the exercise its a laser sensor (<em> Lidar </em> sensor) that takes measures from 0º to 180º on the front side of the car. We will use this sensor to locate the obstacles.

## 2.2. Actuators
As actuators, the robot has motors, those motors let the car move on every direction.

## 3. Software
Firstly, to carry out the VFF algorithm is used a hybrid navegation, so, the API is the one who provides us the global coordinates of the targets the car needs to reach. There is many targets along the circuit that helps the car to complete the lap.

This algorithm is an iterative algorithm whose structure is as detailed:

