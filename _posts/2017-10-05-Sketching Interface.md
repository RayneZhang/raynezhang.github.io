---

layout: post-research
title: "Sketching Interface for Spatial Training Platform"
date: 2017-10-05 15:56:00
categories: Research
tags: Unity WebGL Django
featured_image: '/img/posts/Sketching3.png'
duration: July - Sept 2017
advisor: Wai-Tat Fu
location: Cascade Lab @ UIUC

---

<br />

**MY CONTRIBUTIONS**

In this project, I implemented a free-hand sketching interface, which is the core of the spatial training exercises, and intergreated this interface into the current web platform for training students' visuaospatial skills. Besides this project, I also worked on [another project](/research/2017/10/05/Cubicle.html) during my visit at UIUC.

**TEAMMATES**

Ziang Xiao: Back end development, data analysis.

Yuqi Yao: Front end development, user experience research and design.

<br />

<h3 class="section-title text-center">Introduction</h3>

Due to the importance of visuospatial skill in the field of STEM education, researchers and instructors have put a lot of effort into evaluating and training engineering students’ visuospatial skills. However, previous methods often rely on traditional paper-based questions and face-to-face visuospatial training workshops, which are costly and timeconsuming, especially for large classes. We have designed and evaluated an online platform to provide a low-cost, scalable solution to effectively evaluate and train visuospatial skills, as well as increase students' motivation of continue studying in STEM programs. In addition, the online platform can facilitate the analysis of behavioral and error patterns, which can lead to design of intelligent features that improve learning through the use of adaptive and individualized learning modules.

The free-hand sketching tool allows students to make isometric and multi-view drawings, which are the cores of traning visuospatial skills, using their computer mice. The free-hand sketching tool provides a working area with an isometric dot grid or a dot grid to guide drawing. Students can add or delete a line between two dots without any constraints. The tool also keeps track of students' drawing process step by step. A comprehensive time-stamped log file documenting students' drawing actions will be generated as well for future error pattern analysis. The log file can easily automate the grading process as well.

<br />

<h3 class="section-title text-center">Sketching Interface</h3>

![](/img/posts/sketch/sketching.gif)

**Features**

- Users can join two dots to make a straight line on two types of grids - isometric and orthographic.
- Delete an existing line by clicking the two ends of the line
- Users can draw two types of lines - Solid Line and Dashed Line
- Clear the drawing panel and start over
- Upload the current work to the server
- Download the previous work from the server

I designed and implemented the sketching application independently using Unity. This application is published in webGL and integrated into the existing online spatial training platform. Since the upload/download feature needs development on the server side, I also developed this interface on the server end in Django using techniques of network programming.

<br />

<h3 class="section-title text-center">Spatial Training Platform Overview</h3>

<div class="row auto-clear">
    <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12" align="middle">
        <img src="/img/posts/sketch/home.png">
        <p>Homepage of the platform</p>
    </div>
</div>

<div class="row auto-clear">
    <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12" align="middle">
        <img src="/img/posts/sketch/choice.png">
        <p>a) Multiple Choices</p>
    </div>
</div>

<br />

<div class="row auto-clear">
    <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12" align="middle">
        <img src="/img/posts/sketch/feedback.png">
        <p>b) Feedback Module</p>
    </div>
</div>

<!--<div class="row auto-clear">
	<div class="col-xs-6 col-sm-6 col-md-6 col-lg-6" align="middle">
    	<img src="/img/posts/sketch/choice.png">
        <p>a) Multiple Choices</p>
	</div>
    <div class="col-xs-6 col-sm-6 col-md-6 col-lg-6" align="middle">
    	<img src="/img/posts/sketch/feedback.png">
        <p>b) Feedback Module</p>
	</div>
</div>-->

<div class="row auto-clear">
    <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12" align="middle">
        <img src="/img/posts/sketch/sketch.png">
        <p>c) Sketching Questions</p>
    </div>
</div>

Our online platform is designed to offer a comprehensive assessment and training of visuospatial skills using a set of well-tested multiple choice and free-hand sketching questions. The online platform has two major functions: An interface for answering multiple choice questions and a free-hand sketching tool for answering drawing problems. The interface for the multiple choice questions (Figure a) allows the student to answer questions by clicking on the correct answers, and the system will time-stamped all user actions and automatically determine if the final answers submitted are correct. The platform will also provide feedback (Figure b) to students on their performance. The free-hand sketching tool (Figure c) allows students to make isometric and multi-view drawings (which are the cores of training visuospatial skills) using their computer mice to answer the sketching questions. This platform has 7 weeks of exercises. Currently, my other two teammates (Ziang and Yuqi) are conducting the one-term-long user study at UIUC.

For a complete list of faculty members, previous graduate students and research assistants working on the project, please visit [Cascade Lab](http://cascade.cs.illinois.edu/education.html).