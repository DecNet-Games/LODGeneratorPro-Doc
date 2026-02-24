---
layout: default
title: Batch Processing
parent: Core Features
nav_order: 2
---

# Batch Processing

Optimizing a few hero props is easy. Optimizing a 50,000-object city environment is not. That's why **Batch Processing** is one of the most critical tools in LOD Generator Pro.

Time saving equals money saving. We've built the ultimate "Performance Doctor" so you can fix your whole project in one click.

## Scene-Wide Auto Scan

When you trigger a batch optimize, LOD Generator Pro scans the entire hierarchy for `MeshRenderers` and builds an internal graph of objects that actually need optimization. 

### Size Filtering
Not everything needs an LOD. A tiny soda can model shouldn't have 4 LOD distances—it should just be culled by the camera. The batch engine intelligently skips small meshes automatically based on spatial bounds, saving Editor time and runtime memory.

## Folder Processing

Need to prepare an entire asset pack before making prefabs? 
1. Select a folder in your Project window.
2. Run LOD Generator Pro.
3. It will scan, read the raw asset `.FBX` or `.obj` files, and generate all optimized LOD assets directly into the directory so they are instantly ready for your prefabs.

> **Pro Tip:**
> Check the **Project Optimization Scanner** before batch processing. It displays standard triangle counts, flags heavy meshes, and isolates "No-LOD" objects, acting as a visual heat map for performance hogs!
