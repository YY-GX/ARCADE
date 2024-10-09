---
title: ARCADE Architecture
parent: Framework of ARCADE
layout: page
nav_order: 1
---

<p align="center">
  <img src="assets/images/arch.png" alt="Architecture" style="width:100%;">
</p>

This figure shows the architecture of ARCADE. (I) First, a user provides a single demonstration, $\tau^{AR}$, through AR. (II) We generate a new demonstration, $\tau^{new}$, by following sampled poses, extracted from $\tau^{AR}$, and key poses, obtained via *Key-Poses Detector*. (III) Additional candidate demonstrations are then generated, which are visualized in AR for user validation. Users filter the candidate demonstrations to form an accepted set of generated demonstrations, $\Xi^{accepted}$. (IV) Finally, we continue generating additional new demonstrations, automatically determining whether to keep or discard each demonstration based on comparing it to $\Xi^{accepted}$ via *Automatic Validation*.
