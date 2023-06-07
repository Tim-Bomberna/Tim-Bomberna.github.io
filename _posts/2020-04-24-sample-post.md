---
title: What is CFD? 
layout: post
post-image: "https://raw.githubusercontent.com/thedevslot/WhatATheme/master/assets/images/SamplePost.png?token=AHMQUEPC4IFADOF5VG4QVN26Z64GG"
description: An introduction to the world of computational fluid dynamics.
tags:
- sample
- post
- test
---

# What is CFD? 
Computational fluid dynamics, or CFD, may sound like a complex term, but I assure you it's not. To explain what the term means, let's split it in two. 'Computational' refers to any technique that uses a computer or computer-like system to perform calculations. 'Fluid dynamics' refers to the behavior and movement of fluids. For the human body, we study a special class of fluids, namely 'biofluids'. The most famous biofluid is blood, which flows from the heart through the arteries to the organs, and then flows back through the veins to the heart, where it is re-oxygenized. In cases where we use computer models to calculate how blood flows through an organ of interest, we are performing 'CFD'. 

# What does CFD look like? 
A computer model is a vague term that warrants more explanation. In general, a CFD model is determined by its geometry, its governing equations and its boundary conditions. Let's have a closer look at each of these elements to figure out what constitutes a CFD model. 

## Geometry 
If we want to study blood flow in an artery, our geometry is simply this artery. Usually, we use medical images (CT or MRI) to reconstruct the patient-specific shape of an artery. On a medical image, all tissues appear black or white, or something in-between. If the doctor injects contrast fluid in the artery of interest, the artery will show up in bright white on the medical image, which makes it much easier for us to recognize its shape. The process of annotating the artery on the medical image is called 'segmentation'. Once the segmentation has been done, a 3D-reconstruction of the artery can be made. Usually, this 3D-reconstruction is divided into little elements or blocks. This process is called 'meshing'. The reason why we mesh relates to the next part, the governing equations. 

## Governing equations 
Both blood flow in arteries, oil flow in pipes and airflow in the lungs are governed by the Navier-Stokes equations. By solving these equations, for example, we can calculate the pressure drop along an artery, which tells us something about how easily blood can flow through an artery that might be severely blocked. However, the Navier-Stokes are unsolvable. Therefore, we typically divide the geometry in small sub-domains ('meshing') and approximate the Navier-Stokes equations in each of these domains. The smaller the domains, the more accurate the approximation will be, but the longer the solution will take. The larger the domains, the less accurate, but the overall model will be cheaper. 

## Boundary conditions 
At last, we look at boundary conditions. Since our geometry typically consists only of a part of the human body, we are esentially looking at an isolated problem which, in reality, is not isolated at all. Therefore, our boundary conditions connect our separated geometry to the rest of the 'world' (or body). At the inlet of the geometry, we can prescribe how much blood flows into the geometry. If the artery bifurcates, the geometry will contain multiple outlets, and our boundary conditions can prescribe the blood flow distribution across these outlets. Once our inlet and outlet boundary conditions are set, our computer model will use the Navier-Stokes equations to solve how blood flows between inlet and outlets. 

**Images in the post will look like:**<br>
![Test Image](/WhatATheme/assets/images/1280x720%20Placeholder.png)

**Giphy Gifs will look like:**<br>
<iframe src="https://giphy.com/embed/ZqlvCTNHpqrio" width="480" height="259" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/laughing-despicable-me-minions-ZqlvCTNHpqrio">via GIPHY</a></p>

**YouTUbe Videos will look like:**<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/jTPXwbDtIpA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>