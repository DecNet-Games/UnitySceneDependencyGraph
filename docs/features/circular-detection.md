---
layout: default
title: Circular Dependency Detection
parent: Features
nav_order: 2
---

# Circular Dependency Detection

Circular dependencies (A references B, B references A) are the silent killers of Unity projects. They prevent garbage collection, cause `StackOverflowException` during serialization, and create spaghetti code that is impossible to refactor.

## Automatic Detection
The **Unity Scene Dependency Graph** runs a cycle detection algorithm (DFS-based) every time you scan.

### Indicators
*   Any node involved in a cycle is highlighted in **RED**.
*   The "Details Panel" explicitly warns: `⚠ Circular Dependency detected.`

## Why is this bad?
1.  **Serialization Errors**: Unity's serializer may fail or infinitely loop when trying to save these structures.
2.  **Memory Leaks**: Objects may never be garbage collected because they hold strong references to each other.
3.  **Refactoring Nightmares**: You cannot move Script A to a different assembly without moving Script B, making modular code impossible.

## How to Fix
The tool will pinpoint the cycle. The fix usually involves:
1.  **Interface Segregation**: Create an interface `IBehavior` that A references, instead of referencing B directly.
2.  **Event System**: Use C# Events or `UnityEvent` where A invokes an event that B listens to, breaking the hard link.
