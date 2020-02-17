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

<figure class="align-center">
  <img src="{{ '/assets/images/blog/escenario.png' | absolute_url }}" alt="Figure 1. Scenario.">
  <figcaption>This site Dat URL as an example.</figcaption>
</figure>

## 1.1. What case-based programming is

Case-based control is a relatively simple reactive system. It is an Artificial Intelligence methodology to carry out learning that has achieved good results in many fields of application. As features, a case-based control:
<p>
    · Iterative operation (fast iterations)
</p>
<p>
    · Situation correspondence table
</p>
<p>
    · Allows to react to unforeseen events
</p>
<p>
    · Time does not influence. it's "here and now"
 </p>
    
## 1.2. What PID controller is

[...]


# 2. Image processing

Before implementing the robot intelligence, we must do a **simple image processing** in order to extract the information from the sensors we have been provided. Firstly, we need to get the **RGB** image from the camera, and convert it to **HSV**. Then, what I have done is, using the cv2 library, create a mask with the line colour and aplying it to the HSV image. Now we have a binary image, so we can start extracting information from it.

<figure class="align-center">
  <img src="{{ '/assets/images/blog/rgb.png' | absolute_url }}" alt="RGB image">
  <figcaption>This site Dat URL as an example.</figcaption>
  
  <img src="{{ '/assets/images/blog/hsv.png' | absolute_url }}" alt="HSV image">
  <img src="{{ '/assets/images/blog/binary.png' | absolute_url }}" alt="Binary image">
</figure>

# 3. Case-based implementation

This is the easiest way to perform your logic method. I used an **if-esif** structure contemplating the possible situations in which the car can be involved, I have set the conditions up experimentally.

## 3.1. Way to set the conditions up

I have in account the pixels from my image. I count the rigth and left side pixels from the half of the **binary image**. I count the pixels of the left and right half using the binary image and then apply the most suitable condition for the extracted information from the image.

# 4. PID controller implementation

[...]
