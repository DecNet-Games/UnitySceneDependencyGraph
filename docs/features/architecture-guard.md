---
layout: default
title: Runtime Impact Analysis
parent: Features
nav_order: 3
---

# Runtime Impact Analysis

Understanding the "Cost" of a Prefab before you instantiate it is crucial for mobile and VR development.

## Deep Analysis
The tool doesn't just look at the GameObject. It analyzes the specific assets referenced by the hierarchy:

| Asset Type | Analysis Methodology |
|:---|:---|
| **Texture** | Calculates uncompressed vs compressed detailed size. |
| **Mesh** | Counts Vertices * per-vertex data (Normal, UV, Tangent) size. |
| **Audio** | checks Load Type (DecompressOnLoad vs Streaming) and file size. |

## Memory Budgeting
You can set a **Memory Budget** (e.g., 50MB for a UI panel).
If the total estimated runtime size of a selected node tree exceeds this budget, the node turns **Brown/Dark Orange**, signaling an optimization target.

> [!IMPORTANT]
> The generic size reported in Unity Inspector is often the *file size on disk*. This tool calculates the **Runtime Memory Size**, which is often much larger (e.g., a 2MB JPG might be 16MB in RAM as an uncompressed RGBA32 texture).
