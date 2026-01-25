---
layout: home
title: Home
nav_order: 1
---

# Stop Guessing. Start Visualizing.
{: .fs-9 }

The **Unity Scene Dependency Graph** is the missing link in your Unity workflow. 
Automatically visualize scene references, detect circular dependencies, and estimate runtime memory impact—before you even hit Play.
{: .fs-6 .fw-300 }

[Get Started Now](./docs/getting-started.html){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [View on Asset Store](https://assetstore.unity.com){: .btn .fs-5 .mb-4 .mb-md-0 }
---

## 🛑 The Pain: Hidden Dependencies Kill Projects
Every Unity developer knows the struggle:
*   **"Why is this scene taking 10GB of RAM?"** because a single Prefab referenced a generic list of *everything*.
*   **"StackOverflowException?"** because `GameManager` referenced `UIManager` which referenced `GameManager`.
*   **"Why is the build size 2GB?"** because a test asset was left in a scriptable object resource.

Manual code reviews can't catch these. **The Dependency Graph can.**

## 🚀 The Solution: Visual & Automated Analysis
We provide a dedicated Editor Window that scans your Scene, Prefabs, and Scripts to build a **Directed Acyclic Graph (DAG)** of your project's structure.

### Key Features
*   **🕸️ Visual Node Graph**: Interactive node-based view of your entire scene hierarchy and external references.
*   **🔄 Circular Dependency Detection**: Instantly flag cycles (A->B->A) that cause crashes and serialization loops.
*   **💾 Runtime Impact Estimation**: Predict the memory cost (Textures, Audio, Meshes) of a branch *without* running the game.
*   **📦 Addressables Safety**: Detect synchronous loading of heavy assets on the main thread.
*   **🛠️ One-Click Fixes**: Automated suggestions for texture compression, audio streaming, and breaking cycles.

## ⚡ Quick Links
*   [**Installation Guide**](./docs/installation.html)
*   [**Core Features**](./docs/features/index.html)
*   [**Rules & Best Practices**](./docs/rules/rule-engine.html)

---
> "This tool turned a 2-day debugging nightmare into a 5-minute fix." - *Early Beta Tester*
