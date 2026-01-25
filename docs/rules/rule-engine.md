---
layout: default
title: Rule Engine
nav_order: 5
has_children: true
permalink: /docs/rules
---

# Rule Engine & Auto-Fixes

The **DependencyGraph** includes an intelligent recommendation engine that not only finds problems but offers **One-Click Fixes**.

## Active Rules

### 1. Texture Optimization
*   **Rule**: Textures > 2MB should use `CRUNCH` compression.
*   **Rule**: Very large textures (>4K) are flagged for resizing.
*   **Fix**: Auto-apply compression settings and resize max capability.

### 2. Audio Optimization
*   **Rule**: Audio files > 500KB should use `Streaming` load type to save memory.
*   **Fix**: Tool automatically changes import settings to 'Streaming'.

### 3. Circular Safety
*   **Rule**: No dependency cycles allowed.
*   **Fix**: Manual intervention required (architectural change).

## Using the Fixer
When you select a node with warnings in the Graph:
1.  Look at the **"Recommendations"** section in the right panel.
2.  Click the **[Fix]** button next to the warning.
3.  The tool re-imports the asset with correct settings immediately.
