---
title: Demonstrations Generation
parent: Framework of ARCADE
layout: page
nav_order: 3
---

Generate additional demonstrations by following **sampled waypoints** + **key waypoints** from the single human-derived demonstration.

To obtain **key waypoints**, we propose the `Key-Poses Detector`, which assumes that key waypoints happen in 2 cases:
<div style="display: flex; justify-content: space-between; align-items: center; margin: 0 10%;">

  <img src="../../assets/images/case1.png" alt="Case 1" style="width: 30%; height: auto;">
  <img src="../../assets/images/case2.png" alt="Case 2" style="width: 30%; height: auto;">

</div>

To avoid robot's unnatural behaviors when following waypoints, we include the `User Validation` step where we visualize the generated demonstrations in AR and the user decides to accept or reject.
<div style="display: flex; justify-content: center; align-items: center; gap: 20px;">

  <!-- Video 1 with caption -->
  <div style="text-align: center;">
    <video width="480" height="270" controls>
      <source src="../../assets/videos/accept_case.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p>Accept case (3x speed)</p>
  </div>

  <!-- Video 2 with caption -->
  <div style="text-align: center;">
    <video width="480" height="270" controls>
      <source src="../../assets/videos/reject_case.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p>Reject case (3x speed)</p>
  </div>

</div>

However, validating many demonstrations may still be labor-intensive, even with limited user roles. So we introduce the `Automatic Validation`:
<img src="../../assets/images/algo2.png" alt="case1" style="display: block; margin-left: auto; margin-right: auto; width: 75%;">

