# Object Dataset

The object module of the **INHA-RBY1 Dataset** defines a standardized taxonomy of household objects for RoboCup@Home service robot tasks. It maps objects to public datasets such as YCB, KITchen, HOPE, and GraspNet. All external sources are cited via BibTeX in `sources/citations.bib`.

## Quick Start

```
object/
├── README.md                          ← you are here
├── taxonomy.yaml                      ← object list with metadata
├── sources/
│   ├── citations.bib                  ← BibTeX for all referenced datasets
│   ├── dataset_sources.yaml           ← public dataset registry
│   ├── ycb_mapping.yaml               ← YCB ↔ taxonomy mapping
│   └── kitchen_mapping.yaml           ← KITchen ↔ taxonomy mapping
└── categories/
    ├── dishes.yaml
    ├── drinks.yaml
    ├── fruits.yaml
    ├── snacks.yaml
    ├── foods.yaml
    ├── cleaning_supplies.yaml
    └── toys.yaml
    + task_specific & household defined in taxonomy.yaml
```

## Referenced Public Datasets

14 datasets referenced, grouped by purpose. Full details in `sources/dataset_sources.yaml`, citations in `sources/citations.bib`.

### 6D Pose Estimation
| Dataset | Objects | Key Feature |
|---------|--------:|-------------|
| [YCB](https://www.ycbbenchmarks.com/object-set/) | 77 | RoboCup standard; 3D mesh + RGB-D |
| [KITchen](https://abdelrahmanyounes.github.io/KITchen/) | 111 | Humanoid egocentric, 6D pose |
| [HOPE](https://github.com/swtyree/hope-dataset) | 28 | BOP-compatible household |
| [BOP](https://bop.felk.cvut.cz/) | multi | Unified benchmark (includes T-LESS, YCB-V, LM-O, etc.) |

### Grasp & Manipulation
| Dataset | Objects | Key Feature |
|---------|--------:|-------------|
| [GraspNet-1B](https://graspnet.net/) | 88 | 1.1B grasp poses |
| [DexYCB](https://dex-ycb.github.io/) | 20 | Hand-object interaction |
| [ACRONYM](https://github.com/NVlabs/acronym) | 8,872 | 17.7M grasp labels |
| [Dex-Net](https://berkeleyautomation.github.io/dex-net/) | — | Grasp quality CNN |

### 3D Model Repositories
| Dataset | Objects | Key Feature |
|---------|--------:|-------------|
| [ShapeNet](https://shapenet.org/) | 51K | Largest 3D model repository |
| [Google Scanned](https://app.gazebosim.org/GoogleResearch/fuel/collections/Scanned%20Objects%20by%20Google%20Research) | 1,030 | HD textured 3D scans |
| [OmniObject3D](https://omniobject3d.github.io/) | 6,000 | 190 categories, real-scanned |

### 2D Detection & Segmentation
| Dataset | Key Feature |
|---------|-------------|
| [Open Images V7](https://storage.googleapis.com/openimages/web/index.html) | 600 classes, 16M bboxes, 2.8M masks |
| [OCID](https://www.acin.tuwien.ac.at/en/vision-for-robotics/software-tools/object-clutter-indoor-dataset/) | Indoor clutter segmentation |

### Other
| Dataset | Key Feature |
|---------|-------------|
| [RoboCup@Home](https://github.com/RoboCupAtHome/RuleBook) | Competition rulebook framework |

## Competition Coverage

Objects were selected based on cross-year analysis of RoboCup@Home competitions:

| Year | Location | Objects Used | Overlap with Taxonomy |
|------|----------|-------------:|----------------------:|
| 2023 | France (Bordeaux) | ~42 | 36 |
| 2024 | Netherlands (Eindhoven) | ~40 | 35 |
| 2025 | Brazil (Salvador) | ~37 | 34 |

## Roadmap

The current module provides object taxonomy and mappings to public datasets.
Future releases will include original data captured with the RB-Y1 platform (RGB-D, 3D scans, annotations).

## How to Use

### Load taxonomy in Python
```python
import yaml

with open("object/taxonomy.yaml") as f:
    data = yaml.safe_load(f)

for obj in data["objects"]:
    print(f'{obj["id"]:3d}  {obj["name"]:<25s}  {obj["category"]:<20s}  YCB: {obj["ycb_id"] or "—"}')
```

### Filter by category
```python
fruits = [o for o in data["objects"] if o["category"] == "fruits"]
```

### Get YCB download link
```python
with open("object/sources/ycb_mapping.yaml") as f:
    ycb = yaml.safe_load(f)

for ycb_id, info in ycb["mappings"].items():
    if info.get("download"):
        print(f'{ycb_id}: {info["download"]}')
```

## Citation

If you use this object taxonomy, please cite our dataset and the relevant source datasets:

```bibtex
@misc{inharby1dataset2026,
  title  = {{INHA-RBY1} Object Taxonomy for {RoboCup@Home} Service Robots},
  author = {{Inha-United}},
  year   = {2026},
  url    = {https://github.com/inha-united-athome/inha-rby1-dataset}
}
```

Always cite `inharby1dataset2026` when using any part of this module.
If you use data from a referenced dataset, also cite the original paper — all BibTeX entries are in [`sources/citations.bib`](sources/citations.bib).

## License

Copyright © 2026 Inha-United. Object taxonomy metadata is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
Individual source datasets retain their original licenses — see `dataset_sources.yaml` for details.
