---
layout: post
title:  "Robotics: Line Follower"
description: "My Line Follower proyect in Phyton"
last_modified_at: 2020-02-17
image:
categories: Robotics, Technology
tags: [Robotics, Phyton]
---
# 1. Introduction

For this project I have used CV2 in Phyton for image processing and different logic methods for robots, the robot used has a camera in the front left side of the vehicle (it's a F1 car). First, I have used the most basic of all, case-based programming. The next method of implementation will be through a PID controller. I will be updating this post with the new changes in my proyect.

## 1.1. What case-based programming is

Case-based control is a relatively simple reactive system. It is an Artificial Intelligence methodology to carry out learning that has achieved good results in many fields of application. As features, a case-based control:
    · Iterative operation (fast iterations)
    · Situation correspondence table
    · Allows to react to unforeseen events
    · Time does not influence. it's "here and now"
    
## 1.2. What PID controller is

[...]


# 2. Image processing

Before implementing the robot intelligence, we must do a simple image processing in order to extract the information from the sensors we have been provided. Firstly, we need to get the RGB image from the camera, and convert it to HSV. Then, what I have done is, using the cv2 library, create a mask with the line colour and aplying it to the HSV image. Now we have a binary image, so we can start extracting information from it.

# 3. Case-based implementation

