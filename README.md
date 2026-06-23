# Multi-Robot Disaster Response with Voronoi Coverage (MAE 598 Final Project)

Authors: **Kareena Salim Lakhani, Milan Tiwari**  
---

## Overview

This repository contains the code and report for our 
**multi-robot disaster response using Voronoi-based coverage control** submitted for the class **Multi-Robot Systems** at **Arizona State University**.

We designed a distributed multi-robot control framework based on Voronoi coverage principles. Starting from classical centroid-based coverage control, we extended the model to include dynamic demand fields, finite robot supply capacities, greedy task allocation within Voronoi cells, and collision avoidance through repulsive safety controllers. The system combined continuous coverage objectives with hybrid task-switching behavior to realistically model relief delivery from a single base to multiple hotspots.

A team of ground robots must leave a single base, travel through a
disaster-affected field, and deliver relief supplies to several spatially
distributed demand hotspots. The controller combines:

- **Voronoi coverage control (Lloyd / centroid algorithm)** over a priority
  field and a time-varying demand field.
- A **greedy hotspot task-allocation layer**, which selects and uniquely
  assigns high-demand cells to individual robots.
- A **capacity and refilling model**, so robots must periodically return to
  base when they run out of supplies.
- A **repulsive safety controller**, which maintains a minimum pairwise
  distance between robots.

All simulations are implemented in **MATLAB**.

## Demo Preview

[![ReLIEF-VOR simulation preview](im_gif.gif)](https://github.com/Kareena2207/Multi-Robot_Disaster_Management/blob/main/simulation%3A/Simulation.mov)

The README preview above shows the live disaster-response simulation directly on the main project page. Click the animation to open the full recorded simulation video.

The repository reproduces:

- The **main simulation video / snapshot** with three hotspots (H1–H3),
  robot trajectories, and demand contours.
- The four metric plots:
  - Locational cost vs. time.
  - Total unmet demand vs. time.
  - Coverage served vs. time.
  - Minimum pairwise distance (safety) vs. time.
- The final LaTeX **report PDF** submitted for the course.

---

## Repository structure


```text
.
├── code/
│   ├── main.m
│   ├── initParams.m
│   ├── initState.m
│   ├── runSimulation.m
│   ├── discreteVoronoi.m
│   ├── weightedCentroids.m
│   ├── taskSelection.m
│   ├── safetyController.m
│   ├── visualizeState.m
│   ├── plotMetrics.m
│   └── utils/           
├── report/
│   ├── final_report.pdf
└── README.md
