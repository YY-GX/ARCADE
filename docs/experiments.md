---
title: Experiments
layout: page
nav_order: 3
---

We train vanilla Behavioral Cloning (BC) using demonstrations obtained from ARCADE. We evaluate the learned policy on 3 archetypal tasks: `3-Waypoints-Reach`, `Push`, `Pick-And-Place`. We also evaluate ARCADE on a real household task: `Pouring-Water`, where we achieve `80%` success rate.

<div style="display: flex; justify-content: space-around; align-items: center; gap: 20px;">

  <!-- Video 1 with caption -->
  <div style="text-align: center;">
    <video width="200" height="400" controls>
      <source src="../assets/videos/reach_crop.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p>3-Waypoints-Reach</p>
  </div>

  <!-- Video 2 with caption -->
  <div style="text-align: center;">
    <video width="200" height="400" controls>
      <source src="../assets/videos/push_crop.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p>Push</p>
  </div>

  <!-- Video 3 with caption -->
  <div style="text-align: center;">
    <video width="200" height="400" controls>
      <source src="../assets/videos/pp_crop.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p>Pick-And-Place</p>
  </div>

  <!-- Video 4 with caption -->
  <div style="text-align: center;">
    <video width="200" height="400" controls>
      <source src="../assets/videos/pour_crop.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p>Pour-Water</p>
  </div>

</div>
