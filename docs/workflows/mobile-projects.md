---
layout: default
title: For Mobile Projects
parent: Workflows
nav_order: 1
---

# Workflow: Mobile Optimization

Mobile devices have strict memory limits (often < 2GB available for the app).

## Strategy
1.  **Set a Strict Budget**: In the Settings panel, set your memory budget to **50MB** (or appropriate chunk size).
2.  **Scan Prefabs**: Drag & Drop your main UI Prefabs and Character Prefabs into the window directly to scan them in isolation.
3.  **Runtime Load Check**: Look for **Orange Nodes**. Make sure you aren't loading 50MB of assets via `Resources.Load` at startup.

## Checklist
*   [ ] Analyze the "Main Menu" scene.
*   [ ] Verify no textures are uncompressed RGBA32.
*   [ ] Ensure Background Music is set to Streaming.
*   [ ] Check that common UI sprites are in an Atlas (referenced as one object).
