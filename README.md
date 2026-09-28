# EMBER-3D
### Enhanced Multimodal Base for Electric-Infrastructure Resilience

**EMBER-3D** is an open multimodal 3D dataset designed to support research on
vegetation–electric infrastructure interactions and wildfire resilience.

The initial release is derived from previously collected street-level footage
of utility corridors in **Golden, Colorado, USA**. The dataset connects raw
video observations with extracted keyframes, reconstructed 3D point clouds,
and semantically segmented 3D representations of vegetation and utility poles.

Our broader goal is to establish a reproducible and extensible pathway for
transforming low-cost street-level imagery into AI-ready 3D scientific data
for electric-infrastructure resilience research.

---

<p align="center">
Street-level Footage → Keyframes → 3D Reconstruction → Semantic 3D Representation
</p>

---

## Dataset at a Glance

| Data Component | Status | Description |
|---|---|---|
| Street-level footage | ✅ Available | Ground-based video collected along utility corridors |
| Extracted keyframes | ✅ Available | Frames selected for photogrammetric reconstruction |
| RGB point clouds | ✅ Available | Reconstructed 3D representations of the corridor environment |
| Vegetation point clouds | ✅ Available | Semantically extracted vegetation/tree points |
| Utility-pole point clouds | ✅ Available | Semantically extracted utility-pole points |
| Overhead conductor reconstruction | 🚧 In development | Geometry of overhead conductors and wire spans |
| Georeferencing | 🚧 In development | Transformation from local reconstruction coordinates to geographic coordinates |
| Clearance measurements | 🔬 Planned | Vegetation-to-wire and vegetation-to-infrastructure spatial relationships |
| Standardized metadata | 🔬 Planned | Dataset-level provenance, uncertainty, and quality metadata |

---

## Why EMBER-3D?

Wildfire and infrastructure datasets often describe environmental conditions
at landscape or system scales, while many ignition-relevant interactions occur
at the scale of individual trees, utility poles, and overhead conductors.

Street-level imagery captures these local spatial relationships, but the
information remains largely unstructured in raw image or video form.

EMBER-3D explores a workflow for converting existing street-level observations into:

- spatially explicit 3D geometry,
- machine-readable infrastructure and vegetation features,
- semantically enriched point clouds,
- and ultimately standardized AI-ready data products.

The dataset is intended to support research at the intersection of
**3D computer vision, wildfire resilience, vegetation management, remote sensing,
and electric infrastructure systems**.

---

## Current Data Modalities

### 1. Street-Level Footage

The source data consist of ground-based video collected along utility corridors
in Golden, Colorado.

The footage provides overlapping visual observations of vegetation,
utility poles, overhead infrastructure, buildings, road surfaces, and
surrounding environmental features.

---

### 2. Keyframes

Video frames are sampled and filtered to provide sufficient visual overlap
for structure-from-motion and multi-view reconstruction.

Keyframes preserve the connection between the original visual observations
and the reconstructed 3D environment.

---

### 3. Reconstructed 3D Point Clouds

Photogrammetric reconstruction is used to estimate camera poses and recover
3D scene geometry.

Current processing includes:

- camera pose estimation,
- sparse reconstruction,
- dense reconstruction,
- gravity-axis alignment,
- and scale calibration using independent physical references.

---

### 4. Semantic 3D Point Clouds

Semantic information extracted from the source imagery is mapped back into
the reconstructed 3D environment.

#### Vegetation

#### Utility Poles

This transformation enables individual environmental and infrastructure
components to be analyzed directly in 3D rather than only as image pixels.

---

## Processing Workflow

```text
Previously Collected Street-Level Footage
                    │
                    ▼
             Keyframe Extraction
                    │
                    ▼
          Camera Pose Estimation
                    │
                    ▼
         Sparse / Dense Reconstruction
                    │
                    ▼
        Orientation & Scale Calibration
                    │
                    ▼
         2D Semantic Segmentation
                    │
                    ▼
          2D-to-3D Semantic Mapping
                    │
                    ▼
     Semantically Enriched 3D Dataset