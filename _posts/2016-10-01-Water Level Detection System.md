---
layout: post-project
title: "Automatic Water Level Detection System"
date: 2017-11-20 15:56:00
categories: Projects
tags: Unity HTC-VIVE Virtual-Reality
featured_image: '/img/posts/ComputerVision.jpg'
description: 'Markerless Registration of 3D Object in the HoloLens'

---

This is the capstone project of the course Computer Vision. I led 3 team members to develop a system that can detect water level based on the given image retrieved from the monitor. In this project, I was mainly responsible for retrieving the characteristics of the signes on the water gauge using SIFT and HOG. I also trained the prediction model that can predict the water level using Support Vector Machine(SVM) methods.

<br />

<h3 class="section-title text-center">Image Preprocessing</h3>

To detect the water level, we need to find the water gauge at first, which is in the image preprocess. The image preprocess contains 4 steps: 1) Scale the image to a suitable size. 2) Do the edge detection using different parameters and determine the optimal parameter danamically. 3) Scan the edge image and count the times of black and white stripe. 4) Compute the variance of the times of stripe and determine the cadidate of the water gauge.

![](/img/posts/WaterLevel/PreProcess1.png)

![](/img/posts/WaterLevel/PreProcess2.png)

<br />

<h3 class="section-title text-center">Water Level Detection</h3>

To count the number of "E" on the water gauge, which is equivalent to detecting the water level, I first retrieve the HOG characteristic from the positive and negative sample sets, and then import them to SVM for training. After training with SVM, a predicting model is obtained to detect the pattern of "E" in the image of the given water gauge. At last, we can compute the exact water level by counting the number of "E" in the column that contains the most "E".

![](/img/posts/WaterLevel/Result.png)