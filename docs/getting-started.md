---
layout: default
title: Getting Started
nav_order: 2
---

# Getting Started

Welcome to **LOD Generator Pro**. Stop losing players because of unstable FPS and massive WebGL build sizes. LOD Generator Pro allows you to optimize your meshes in just 3 clicks with automated, non-destructive mesh simplification.

## What is LOD Generator Pro?

Level of Detail (LOD) optimization is critical for game performance. As objects move further away from the camera, they require fewer polygons to render convincingly. By swapping high-poly models for lower-poly versions, you massively save on:
- **Triangle Count**
- **GPU Memory**
- **Draw Calls & Vertex Processing**

LOD Generator Pro provides:
- One-click LOD generation
- Visual diffing (Before vs After)
- Safe, non-destructive workflows (auto duplicate)
- Automatic Screen-Relative Tuning for Mobile, PC, VR, and Console.

## Core Concepts

Understanding how LOD Generator Pro works will help you get the most out of your optimization workflow.

### 1. Smart Vertex Clustering
LOD Generator Pro uses an advanced spatial Vertex Clustering algorithm under the hood. Unlike simple percentage-based decimation that ruins hard edges and destroys UVs, clustering safely merges nearby vertices while preserving texture coordinates and vertex normals through intelligent averaging.

### 2. Batch Processing
Tired of clicking on every single prefab in your scene? The **Batch Optimizer** scans your hierarchy or folder structures, filters out meshes that are already too small to matter, and applies optimization globally.

### 3. Automatic LOD Groups
When generating LODs, Unity's built-in `LODGroup` component is automatically attached and configured with standard transition thresholds depending on your selected target platform.

[Install LOD Generator Pro]({{ site.baseurl }}/docs/installation){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 }
