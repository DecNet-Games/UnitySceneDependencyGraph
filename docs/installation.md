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

## 1. Purchase & Download
The Usage of **Unity Scene Dependency Graph** requires a license from the Unity Asset Store.

1.  Visit the **[Unity Asset Store Page](https://assetstore.unity.com)**.
2.  Purchase and Add the asset to your library.
3.  Open your Unity Project.

## 2. Import into Unity
1.  In Unity, verify you are using a supported version (**2021.3 LTS** or higher).
2.  Go to **Window > Package Manager**.
3.  Select **Packages: My Assets** from the top-left dropdown.
4.  Search for **"Scene Dependency Graph"**.
5.  Click **Download** (if not already downloaded).
6.  Click **Import**.
7.  In the Import window, ensure all files are checked and click **Import** again.

## 3. Launching the Tool
Once the import is complete, the tool will automatically compile.
You can access it via the menu:

*   **Tools > Dependency Graph Analyzer > Open Graph Window**

![Menu Location](/assets/images/menu_loc.png)

---

## Troubleshooting Import
If you see any errors after importing:
*   **Namespace Conflicts**: Ensure you don't have another folder named `DependencyAnalyzer` in your project.
*   **Version Mismatch**: If using Unity 6000+, ensure you have the latest update from the Asset Store.

> [!NOTE]
> This tool does not have any external DLL dependencies. It uses pure C# and Unity's UIElements API.
