---
layout: default
title: Quick Start
nav_order: 4
---

# Quick Start: Hello World Usage

Let's optimize your first mesh! In just one minute, you'll see why LOD Generator Pro is universally loved by developers tired of manual labor.

## 1. Open the Generator Window
1. Navigate to your top menu bar in Unity.
2. Click `Tools > LOD Generator Pro > Optimizer Window` (or use the equivalent menu path depending on your Unity version).

## 2. Select a Target Mesh
1. Select a GameObject in your scene that contains a `MeshFilter` and a `MeshRenderer`.
2. Notice that the LOD Generator Pro window instantly populates with the **Diff Preview**. This shows your current triangle count and memory estimate.

## 3. Generate LODs
1. Choose your Target Platform (Mobile, PC, VR, Console) from the dropdown. This automatically tunes the LOD Group's screen-transition thresholds.
2. Click the **Generate LODs** button.

## What just happened?
LOD Generator Pro performed the following completely automatically:
1. Created **Duplicate Meshes** (Safe Mode means your original mesh assets are untouched).
2. Performed **Vertex Clustering Simplification** to create LOD1, LOD2, and LOD3.
3. Added a `LODGroup` component to your object.
4. Assigned LOD0 (original), LOD1 (70%), LOD2 (40%), and LOD3 (15%) to the appropriate transition boundaries.

> **Pro Tip:**
> Move your Scene View camera back and forth. You will see the mesh transition smoothly between high-detail and low-detail versions, saving performance when zoomed out!
