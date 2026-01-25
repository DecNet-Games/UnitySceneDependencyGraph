---
layout: default
title: FAQ
nav_order: 7
---

# Frequently Asked Questions

### Q: Does this work with ECS / DOTS?
**A:** Currently, the tool focuses on `MonoBehaviour` and GameObject hierarchies. ECS entities are not fully supported in the graph visualization yet.

### Q: Can I export the graph to an image?
**A:** Not directly to an image file, but you can export the data to JSON/CSV (via Toolbar) and visualize it in third-party tools like graphviz if needed.

### Q: Is this tool safe to run during Play Mode?
**A:** Yes! If you enable "Auto-Refresh", it will track dependencies as they spawn. However, for massive scenes, this may impact frame rate. We recommend scanning in Edit Mode or pausing Play Mode to scan.

### Q: Why is my specific script reference not showing?
**A:** The tool relies on Unity's `SerializedObject` system. If you are using private fields without `[SerializeField]` or pure C# classes not attached to GameObjects, they might not appear in the Scene graph.

### Q: I found a bug!
**A:** Please open an issue on our [GitHub Repository](https://github.com/DecNet-Games/UnitySceneDependencyGraph/issues).
