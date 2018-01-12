---
layout: post-research
title: "Assembly Assitance in Augmented Reality (On-going)"
date: 2017-11-20 15:56:00
categories: Research
tags: AugmentedReality MixedReality HoloLens
featured_image: '/img/posts/Assembly.jpg'
duration: Oct 2017 - Now
advisor: Xubo Yang
location: Digital ART Lab @ SJTU

---

<br />

**MY CONTRIBUTIONS**

I worked on the AR Assembly Assistance project as an independent researcher and developer at the Digital ART Lab, Shanghai Jiao Tong University. I was responsible for the object-based markerless registration in the HoloLens. I also designed and implemented the virtual instructions in the HoloLens and interactions using voice commands and gestures.

<br />

<h3 class="section-title text-center">Introduction</h3>

Object registration is always a key component in numerous Augmented Reality (AR) applications. As one of the most prominent AR headsets on the market, the Microsoft HoloLens has demonstrated strong portability and novel 3D hologram-like interfaces. However, since the HoloLens does not provide real-time, high resolution depth data, the registration process is severely limited to marker-based registration or employing external devices. In this project, I mainly address the problem of markerless registration of a 3D object solely in the HoloLens by implementing an efficient template-matching algorithm in the image space. A set of 2D edge templates of an object are employed to match a query image. My study focuses on industrial objects, which are mostly textureless, and the method has been tested on real environment, showing its efficiency, robustness and convenience.

<br />

<h3 class="section-title text-center">System Overview</h3>

Task guidance has been an active topic in the field of augmented reality (AR), with applications to a wide range of domains, including operations, assembly, maintenance, etc. Seeing instructional graphics overlaid directly on the actual task environment can significantly improve a user's understanding compared to viewing instructions displayed on a nearby monitor or in a paper manual. AR technology enables a tech/worker to directly interact with the local environment for 3D spatial referencing and action demonstration and allows the user to visualize instructions directly overlaid on the environment. In our system, we propose an approach where a senior engineer makes the graphic animations on the computer in advance and a local tech/worker accomplishes the assembly task according to the virtual instructions overlaid on the environment wearing the Microsoft HoloLens.

![](/img/posts/Assembly/Overview.png)

My work lays on the local tech/user side, where I mainly developed the object registration, the graphic interface, the animation display and the interactions using voice commands and gestures. Since this is a project cooperated with Shanghai General Motor Company and the pictures of the motor are confidential, we can only show the pixelated pictures. To better illustrate my research, I will use another model for the following demonstration.

<br />

<h3 class="section-title text-center">Markerless Object Registration in the HoloLens</h3>

To augment object-specific virtual instructions in the HoloLens, first of all we need to find the 3D location and 3D pose/rotation of the motor in the real environment. A disadvantage of the Microsoft HoloLens is that real-time, high resolution depth data provided by HoloLens depth sensor is not accessible. The HoloLens does have spatial mapping functions, however mesh and vertices generated are not accurate enough for detailed 3D information. This disadvantage severely impedes the development of many 3D registration methods such as ICP algorithm. Due to this limitation, the state-of-the-art HoloLens applications use markers for object registration or register based on plane recognition instead of an object specific registration. One way to bypass the limitation is by utilizing external depth sensors such as Kinect or RealSense. However, these methods entailed complicated devicesetup and lost the system portability.

In the past decades, people have employed texture information, feature points and shape for object recognition and registration. For textureless industrial objects, the methods of utilizing texture information or feature points may not be effective. On the other hand, edge or contours are invariant to general geometric transformations and illumination changes, and therefore suitable for recognizing and registrating 3D textureless objects.

In this project, I implemented an image-based markerless registration method using the HoloLens in order to augment object-specific information(virtual instructions) into real environment(motors). I first generate edge templates of the 3D object seen from a number of viewpoints. Then I implement the Chamfer Matching algorithm between the templates and the edge map of the image. Since the starting pose of the object is unknown, the searching for the best alignment in the huge 6D pose space is extremely time-consuming, I employ techniques such as image down sampling to reduce time cost of the matching algorithm. I also propose several reasonable assumptions based on practical condition.

The figure below shows the flowchart of the registration process.

![](/img/posts/Assembly/Diagram.png)

#### Assumption

In this project, We assume that each physical object has a virtual replica, named digital models. We will use a model of a female body in the following demonstration.

![](/img/posts/Assembly/Assumption.png)

<br />

#### Offline Templates Generation

[To Be Updated]

<br />

#### Edge Extraction

[To Be Updated]

<br />

#### Chamfer Matching

[To Be Updated]

<br />

#### Results

The image-based registration method has been tested on a model of Female Body using the HoloLens. The target model with the height of 30cm and the width of 15cm is made of curved and complex shapes. This model is impossible to register using the low resolution depth data provided by the HoloLens. We have the corresponding 3D digital model of the same size and generated 1620 off-line edge templates of each resolution level using the digital model. The original resolution of the captured image of the HoloLens is 1280 x 720. We have successfully augmented the model with the digital one, showing its convenience. Figures below show the results of the registration task on poses and details from different angles.

![](/img/posts/Assembly/Results.png)

![](/img/posts/Assembly/Details.png)

As you can see in the pictures of details, the 6D pose estimation is not so accurate. Whether the accuracy is desirable for virtual instructions in the HoloLens is still under research. In addition, the registration process is not real-time (about 1min) so I am still seeking to optimize the process. For more details about the implementation or the project, please feel free to contact me.