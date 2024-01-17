---
title: "Incorporating Metric Depth Learning into Neural Radiance Fields"
date: 2023-12-18
tags: ["NeRF", "Neural Networks", "Python", "TensorFlow", "3D Reconstruction", "Deep Learning"]
author: ["Lechen Zhang"]
description: "ECBM 4040 Course Project at Columbia University, Supervised by Prof. Zoran Kostić, 2023." 
summary: "ECBM 4040 Course Project at Columbia University, Supervised by Prof. Zoran Kostić" 
cover:
    image: "depth.gif"
    alt: "Image caption"
    relative: false

---

---

## Abstract

Neural radiance fields (NeRF) encode a scene into a neural representation that enables photo-realistic rendering of novel views. Neural However, a successful reconstruction from RGB images requires a large number of input views taken under static conditions — typically up to a few hundred images for room-size scenes, and the prediction of volume density is usually not as accurate as the RGB, which leads to ghostly artifact issues. To address this issue, a metric depth learning module is incorporated with the classic NeRF framework to leverage the depth prior for faster training speed and better rendering quality.

---

## Overview of the Architecture

![](nerf.drawio.png)

---

## Loss Function

$$
L=L_{rgb}r+\lambda_dL_{Depth}
$$
where $\lambda_d$ represents the weight of $L_{Depth}$.

---

## Results

Reconstructed model's depth map with depth learning prior(Proposed):

![](withdepth.jpg)

Reconstructed model's depth map without depth learning prior(Original NeRF):

![](wtdepth.png)

Final Rendering Results:

![](depth_test.gif)


