---
layout: default
title: The 'Bad Core' Rule
parent: Rule Engine
nav_order: 2
---

# The "Bad Core" Architecture Rule
{: .fs-9 }

One of the most common architectural mistakes in Unity projects is the **"Upward Dependency"**.

## The Concept
Your code should flow continuously **Downwards**:
*   `Gameplay` depends on `Core` -> ✅ Good.
*   `Core` depends on `Gameplay` -> ❌ **BAD**.

If your `Core` utilities (like `SoundManager`) need to reference specific Gameplay elements (like `PlayerController`), you have created a "Bad Core" dependency.

## Why is it blocked?
1.  **Portability**: You can't take your `Core` folder to a new project because it drags the specific game logic with it.
2.  **Compilation Times**: Changing the Player script forces the entire Core assembly to simple recompile.

## Enforcement
The Dependency Graph visualizes these layers. If you see arrows pointing "Up" from your foundation systems to your implementation layer, you have violated the Bad Core rule.

> [!TIP]
> Use abstract classes or Actions (`System.Action`) to let Core communicate with Gameplay without referencing it directly.
