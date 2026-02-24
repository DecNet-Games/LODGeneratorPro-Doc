---
layout: default
title: Mesh Simplification
parent: Core Features
nav_order: 1
---

# Automatic Mesh Simplification

The heart of LOD Generator Pro is its custom Mesh Simplification engine. 

Most traditional simplifiers use random edge-collapse algorithms that can totally destroy the topology of your mesh, leaving you with broken UVs and smoothed-out hard edges. LOD Generator Pro avoids this by taking a **Vertex Clustering** approach.

## How it works

The engine creates a 3D grid around the target mesh. The grid size is controlled by a built-in `Quality` parameter (ranging from High Quality `0.9` down to Low Quality `0.1`). 

Vertices that fall into the same grid cell are mathematically clustered and welded together. 

### Why Vertex Clustering?
- **Preserved Normals**: The algorithm intelligently averages the surface normals of the clustered vertices, preserving hard edges far better than recalculating from scratch.
- **UV Safety**: Texture coordinates are averaged proportionately so that your unwrapped UVs don't warp destructively.
- **Speed**: It is incredibly fast compared to iterative edge-decimation, making it perfect for Unity Editor-time batch operations.

## Fallback Mechanisms
To guarantee that you never end up with an invisible mesh, if the algorithm detects that the simplification is too aggressive and results in 0 triangles, it will automatically fall back and preserve the original geometry.

> **Pro Tip:**
> Want to be extremely careful? LOD Generator turns on **Safe Mode** by default. This ensures any modifications are performed on auto-instantiated duplicates of your mesh (e.g., `MeshName_LOD1`), never destructively modifying your original FBX or `.asset` files.
