---
layout: post
title:  "Robotics: drone_cat_mouse exercise"
description: "My drone_cat_mouse proyect in Phyton"
last_modified_at: 2020-02-17
image:
categories: Robotics, Technology
tags: [Robotics, Phyton, cv2]
---

# 1. Introduction

For this project I have used CV2 in Phyton for image processing and different logic methods for robots, the robot used has a camera in the front side of the drone (the black one). The objective is that the black drone (cat) needs to follow the red one (mouse) in an open field map.

<figure class="align-center">
  <img src="{{ '/assets/images/blog/drone_scenario.png' | absolute_url }}" alt="Figure 1. Scenario.">
</figure>

# 2. Image processing

First of all I needed to proccess the image that i was getting from the front camera. I tryed with many color spaces and tones. But for me, no one worked, so I used the one provided by the exercise theory. After converting the image into HSV I applied a binary threshold to it and then I got the contours from it (using the findContours() method from cv2). With the contour array I get the areas and then I keep the biggest one (it is suposed to be the drone) and calculate the X and Y errors. This is the processed image:

<figure class="align-center">
  <img src="{{ '/assets/images/blog/img_processed.png' | absolute_url }}" alt="Figure 2. Processed image.">
  <figcaption>Processed image.</figcaption>
</figure>

# 3. Following method

I applied a case-based method in order to follow the "cat", setting the movement speed experimentally. The first try, I implemented an algorithm that the drone was moving based on the area it calculated on the red one, but this area was too small and the drone was very slow so I needed to improve it. This is an example execution of the algorithm:

<pre>
<div align="center">
<div class="”video-responsive”">
<iframe width="560" height="315" src="https://www.youtube.com/embed/ObeuCfV-d3k" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>
</pre>

I improved the algorithm considering many cases with the area value. And I got this result:

<pre>
<div align="center">
<div class="”video-responsive”">
<iframe width="auto" height="315" src="https://www.youtube.com/embed/ccqvlLJKluw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>
</pre>

As you can appreciate in the last video, the drones had a collision so I adjusted some parameters in order the drones don't collide. So this is the third version of my exercise with a total of 397.0 points:

<pre>
<div align="center">
<div class="”video-responsive”">
<iframe width="auto" height="315" src="https://www.youtube.com/embed/VjX5CmVBcm8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>
</pre>




