---
layout: default
title: Dependency Graph
parent: Features
nav_order: 1
---

# Visual Dependency Graph

The heart of the tool is the **Graph View**. Built on Unity's UIElements and GraphView API, it provides a zoomable, pannable map of your project's architecture.

## How it Works
The analyzer recursively reflects over all `MonoBehaviour` scripts and `SerializedObject` properties in your scene roots.
It traces:
*   Direct References (Inspector slots)
*   Lists and Arrays
*   Unity Events
*   Runtime Reference lookups (`GetComponent`, etc. - *Experimental*)

## Graph Navigation
*   **Scroll Wheel**: Zoom In/Out
*   **Middle Mouse / Alt+Drag**: Pan
*   **Click**: Select Node
*   **Drag Element**: Rearrange nodes layout

## Filtering & Search
(Coming Soon)
You can filter the graph to show only specific layers (e.g., "UI Only" or "Gameplay Only") to reduce noise in large scenes.
