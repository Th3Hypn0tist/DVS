# DVS — Data Visualizer Studio

DVS is a generic S3D-backed data-visualization subsystem originally developed inside LMTS.

This repository preserves the LMTS extraction baseline before DVS is removed from the LMTS core. The original LMTS namespace and integration files are intentionally retained in this first snapshot so the extraction is lossless and auditable. DVS can be decoupled into its own standalone package later without changing the historical baseline.

## Extraction baseline

Source project: `Th3Hypn0tist/LMTS`

Source branch: `feature/tui-user-profile-restructure`

Source commit: `8267c0f847825b68d41573b2616916fc7955377c`

The snapshot contains:

- DVS core model, registry and runtime
- Input Templates and Visualization Presets
- Studio and Visualizer
- S3D bridge
- report-source and LMTS telemetry adapters
- Python host
- LMTS service/settings integration
- DVS tests

The 3D visualization subsystem is no longer required by LMTS itself, but DVS remains useful as an independent system and is preserved here for future development.

## Baseline architecture

```text
formal source format
    -> Input Template
    -> typed projection
    -> Visualization Preset
    -> visual plan
    -> S3D
```

For the detailed baseline contract and implementation notes, see `lmts/dvs/README.md`.
