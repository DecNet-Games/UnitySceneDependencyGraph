---
layout: default
title: Installation
parent: Home
nav_order: 2
---

# Installation
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Requirements
*   **Unity Version**: 2021.3 LTS or higher (Tested on 2022.3, 6000.0).
*   **OS**: Windows / macOS / Linux.
*   **Dependencies**: None (Uses `UnityEngine.UIElements` built-in).

## Option 1: Install via UPM (Git URL) - Recommended
The easiest way to install and keep updated is via the Unity Package Manager.

1.  Open Unity Project.
2.  Go to **Window > Package Manager**.
3.  Click the **+** (plus) icon in the top left.
4.  Select **"Add package from git URL..."**.
5.  Paste the repository URL:
    ```
    https://github.com/DecNet-Games/UnitySceneDependencyGraph.git
    ```
6.  Click **Add**.

## Option 2: Manual Installation
If you prefer to include the source code directly in your project:

1.  Download the latest [Release](https://github.com/DecNet-Games/UnitySceneDependencyGraph/releases).
2.  Extract the ZIP file.
3.  Copy the `Assets/UnitySceneDependencyGraph` folder into your project's `Assets/` directory.

## Option 3: Unity Package
1.  Download the `.unitypackage` from the [Releases Page](https://github.com/DecNet-Games/UnitySceneDependencyGraph/releases).
2.  Double-click the file while your project is open.
3.  Click **Import**.

---

> [!NOTE]
> Ensure you do not have conflicting folder names if installing manually. The tool lives under the `DependencyAnalyzer` namespace.
