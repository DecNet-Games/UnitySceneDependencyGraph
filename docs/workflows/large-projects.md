---
layout: default
title: For Large Scale Projects
parent: Workflows
nav_order: 2
---

# Workflow: Large Scale & Team Projects

For projects with 10+ developers or >10GB of assets.

## CI/CD Integration
You can run the analyzer as part of your Jenkins / GitHub Actions pipeline.
Use the command line argument to run the scan and fail the build if circular dependencies are found.

```bash
Unity.exe -batchmode -executeMethod DependencyAnalyzer.Integ.BuildHooks.AnalyzeAndExit -projectPath .
```

## Snapshot Comparison
1.  **Baseline**: Validated a "Good" build? Save a Snapshot (`.json`) of the graph. Commit this to Git.
2.  **Review**: Before merging a Pull Request, load the "Snapshot" and compare it with the current branch.
3.  **Detect**: The tool will highlight *New Nodes* in Green and *Deleted Nodes* in Red.
    *   *Did the PR accidentally add a reference to a 4K texture?*
    *   *Did it unexpectedly link the Inventory System to the Audio System?*

Use this to gatekeep your architecture quality.
