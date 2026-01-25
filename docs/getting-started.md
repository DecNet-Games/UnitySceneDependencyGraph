---
layout: default
title: Getting Started
parent: Home
nav_order: 3
---

# Getting Started
{: .no_toc }

This guide will get you from zero to analyzing your first scene in under 60 seconds.

## 1. Open the Window
After installation, the tool is available in the top menu bar.

*   Go to **Tools > Dependency Graph Analyzer > Open Graph Window**.

![Menu Location](/assets/images/menu_loc.png)
*(Note: Screenshot placeholder)*

## 2. Scan Your Active Scene
1.  Open the scene you want to analyze in the Unity Editor.
2.  In the *Dependency Analyzer* window settings (top toolbar), click **Scan Scene**.
3.  Wait for the analysis to complete (usually < 2 seconds).

## 3. Interpreting the Graph
Once scanned, you will see a node-based representation of your scene.

*   **Nodes**: Represent GameObjects, Scripts, or Assets (Textures, Meshes).
*   **Edges (Lines)**: Represent references (e.g., `Player` holds a reference to `SwordPrefab`).

### Node Colors
*   **White/Grey**: Standard GameObject or Script.
*   **🔴 Red**: Part of a Circular Dependency (Critical Issue).
*   **🟠 Orange**: Runtime Loaded (Resources/Addressables).
*   **🟤 Brown**: Heavy Asset (Exceeds current Memory Budget).

## 4. View Details
Click on any node to open the **Inspector Panel** on the right side of the window.
Here you will see:
*   **Memory Estimation**: How much RAM this branch costs.
*   **Reference Count**: How many objects mistakenly point to this.
*   **Recommendations**: Auto-fix buttons for identified issues.

> [!TIP]
> Use the **"Simulate Removal"** button in the details panel to see which other parts of your project would break if you deleted this asset.
