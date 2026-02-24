---
layout: default
title: LOD Group Setup
parent: Core Features
nav_order: 3
---

# Automatic LOD Group Setup

The biggest frustration with LODs isn't making the meshes—it's assigning them to the `LODGroup` component and endlessly tweaking the screen relative transition heights.

LOD Generator Pro completely automates this step with built-in Platform Profiles.

## Auto-Configuration

When LOD Generator Pro simplifies a mesh:
1. It adds the official Unity `LODGroup` component.
2. It assigns `LOD0` (Original: 100%), `LOD1` (70%), `LOD2` (40%), and `LOD3` (15%) to the array.
3. It calculates transition thresholds depending on what platform your build is targeting.

## Platform Profiles

Different platforms have different processing capabilities and physical screen sizes. You don't want a mobile VR headset transitioning LODs at the same distance as a 4K PC monitor.

LOD Generator Pro provides instant configuration presets:
- **Mobile Low / High**: Aggressive early culling, switching to low-poly models very close to the camera.
- **PC Ultra**: Pushes LODs further out to prioritize visual fidelity.
- **VR**: Extremely tuned transitions to prevent "popping" meshes while keeping 90/120Hz framerates.
- **WebGL Lite**: Maximum compression logic meant to remove invisible geometry entirely.

> **Pro Tip:**
> Want to change your mind later? You can switch the active Platform Profile and LOD Generator Pro will re-auto-configure your LOD Groups instantly across the scene!
