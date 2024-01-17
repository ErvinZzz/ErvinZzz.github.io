---
title: "Implicit Neural Evolution with LLM Supervision"
date: 2023-12-01
tags: ["CUDA", "Neural Networks", "Evolutionary Algorithm", "Soft Robot", "LLM"]
author: ["Lechen Zhang"]
description: "MECS 4510 Course Project at Columbia University, Supervised by Prof. Hod Lipson, 2023." 
summary: "MECS 4510 Course Project at Columbia University, Supervised by Prof. Hod Lipson" 
cover:
    image: "soft.png"
    alt: "Image caption"
    relative: false

---

---

## Overview

![](soft1.png)

---

## CUDA-Accelerated Physics Simulation

An optimized memory management strategy inspired by Boxi Xia's [work](https://github.com/boxiXia/FlexipodFast) is utilized to accelerate the physics simulation. The property array of the struct is allocated separately in GPU, which enables more efficient memory management and lower memory consumption.

![](soft9.png)

Energy Conservation Test for the simulator, shows the accuracy of the simulation.

![](soft7.png)

---

## CUDA-Accelerated Implicit Encoding and Neural Evolution

A Multi-Layer Perceptron (MLP) is utilized to implicitly encode the soft robot morphology and control. 

![](soft2.png)

![](soft3.png)

The matrix calculation for the forward propagation in the neural evolution is also accelerated by CUDA.

![](soft8.png)

---

## Large Language Model Supervision

The hyperparameter tunning for the evolutionary algorithm is considered a time-consuming problem. However, the recent Large Language Models (LLMs) like [GPT-4 Turbo](https://platform.openai.com/docs/models/gpt-4-and-gpt-4-turbo) provide a huge context window that enables the possibility of using LLMs to supervise the evolution process of the evolution algorithm and adjust the hyperparameter of the EAs dynamically. 
![](soft4.png)

The experiment is conducted using GPT-4 Turbo API and the results shows that the diversity is better maintained.

![](soft5.png)

---

## Results 

[![Demo Video](https://markdown-videos-api.jorgenkh.no/url?url=https%3A%2F%2Fyoutu.be%2FdExNs8Zm6PI)](https://youtu.be/dExNs8Zm6PI)

---

## Related material

+ [Code on Github](https://github.com/ErvinZzz/soft_evolution)
+ [Presentation slides](pre.pdf)