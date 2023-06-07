---
title: Intro to CFD 2 - What is metamodelling? 
layout: post
post-image: ./assets/images/catheter.png
description: This is an introduction to AI-enabled metamodelling.
tags:
- artificial intelligence
- computational fluid dynamics
- metamodelling
---

# The cost of a simulation 

Metamodels are hugely popular in computer modelling research. There's an obvious reason for that: CFD models can be computationally expensive, requiring hours or even days to perform a single physically realistic simulation of a biological process. Often, we need more than one simulation. For example, if we are modelling a treatment, and want to investigate the impact of a clinically variable parameter (such as implant size or injection site), we need to run multiple CFD simulations to be able to compare the outcomes against other. Otherwise, if we want to figure out how sensitive the output of our CFD simulations towards some model-related input parameters (such as boundary conditions or material properties), we need to run many CFD simulations with slight variations in the input parameters to be able to quantify the impact on the output distribution. Hence, if single CFD simulations are costly, running many CFD simulations for pretreatment planning or sensitivity analysis, is even much more computationally costly. Often we do not have enough time, or resources. And that's why we turn to metamodels. 

# What is a metamodel? 
'Meta' is a Greek suffex that means to refer to itself. For example, a metajoke is a joke about a joke. And that makes a metamodel a model of a model. Here, we aim to replace the computationally expensive CFD simulation by a much cheaper metamodel. The cheap metamodel allows to run many more 'simulations' (or rather, simulations of simulations) in a specific time period. This makes them very interesting for the examples of sensitivity analysis and pretreatment planning as given above. 

# How do you construct a metamodel? 
Often, we employ artificial intelligence (AI) techniques to construct such metamodels. Generally, an AI algorithm learns a relationship between input and output based on specific input-output pairs. Once the relationship is known, the algorithm can be simply used to transform new inputs into new outputs without running the original, computationally heavy simulation. Hence, the first thing we need is to generate enough input-output pairs using the original model to be able to construct that relationship. What that relationship looks like, depends highly on the technique chosen. Popular metamodel techniques are polynomial chaos expansion and Gaussian processes, but many others can be tried. 
