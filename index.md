---
title: Home
layout: home
nav_order: 1
---

# ARCADE: Scalable Demonstration Collection and Generation via Augmented Reality for Imitation Learning
Yue Yang, Bryce Ikeda, Gedas Bertasius, Daniel Szafir

[Website](https://yy-gx.github.io/ARCADE){: .btn .btn-outline }
[Paper](https://drive.google.com/file/d/1batts1Ac293R3WA06qmrZxrvNFUm-Z74/view?usp=drive_link){: .btn .btn-outline }
[Code](https://github.com/YY-GX/ARCADE-Codebase){: .btn .btn-outline }


## Abstract
Robot Imitation Learning (IL) is a crucial technique in robot learning, where agents learn by mimicking human demonstrations. However, IL encounters scalability challenges stemming from both non-user-friendly demonstration collection methods and the extensive time required to amass a sufficient number of demonstrations for effective training. In response, we introduce the **A**ugmented **R**eality for **C**ollection and gener**A**tion of **DE**monstrations (**ARCADE**) framework, designed to scale up demonstration collection for robot manipulation tasks. Our framework combines two key capabilities: 1) it leverages AR to make demonstration collection as simple as users performing daily tasks using their hands, and 2) it enables the automatic generation of additional synthetic demonstrations from a single human-derived demonstration, significantly reducing user effort and time. We assess ARCADE's performance on a real Fetch robot across three robotics tasks: _3-Waypoints-Reach_, _Push_, and _Pick-And-Place_. Using our framework, we were able to rapidly train a policy using vanilla Behavioral Cloning (BC), a classic IL algorithm, which excelled across these three tasks. We also deploy ARCADE on a real household task, _Pouring-Water_, achieving an 80% success rate. 


## Introduction Video
<video width="960" height="540" controls>
  <source src="assets/videos/intro_video.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
