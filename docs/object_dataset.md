---
title: Object Dataset
---

# Object Dataset

The **Object Dataset** module provides a curated taxonomy of household objects for RoboCup@Home service robot tasks, mapped to **18 public datasets** with full academic citations.

!!! info "Design Philosophy"
    We build a **hybrid dataset**: original RGB-D captures from our RB-Y1 humanoid, plus curated mappings to established public datasets (YCB, KITchen, HOPE, GraspNet, etc.). All external sources are properly cited via BibTeX.

---

## Object Categories

| Category | Count | Example Objects |
|----------|------:|-----------------|
| :fork_and_knife: Dishes & Cutlery | 10 | bowl, plate, cup, fork, knife, spoon |
| :cup_with_straw: Drinks | 12 | coke, milk, orange juice, Red Bull |
| :apple: Fruits | 12 | apple, banana, lemon, orange, pear |
| :cookie: Snacks | 12 | Pringles, cornflakes, chips, crackers |
| :canned_food: Foods & Condiments | 16 | tuna, ketchup, mustard, sugar, soup |
| :sponge: Cleaning Supplies | 10 | sponge, cloth, soap, Colgate |
| :jigsaw: Toys | 8 | Rubik's cube, tennis ball, dice |
| :gear: Task-Specific | 10 | bag, laundry basket, T-shirt |
| :house: Household | 10 | book, remote, tissue box, scissors |

---

## Source Datasets

We reference **18 public datasets** — each with proper BibTeX citations in `sources/citations.bib`.

### 3D Models & Point Clouds

| Dataset | Objects | Key Feature | Citation |
|---------|--------:|-------------|----------|
| **YCB** | 77 | RoboCup standard; 3D mesh + RGB-D | Calli et al., 2015 |
| **BigBIRD** | 125 | 600 RGB-D views per object | Singh et al., 2014 |
| **Google Scanned** | 1,030 | HD textured 3D scans | Downs et al., 2022 |
| **ShapeNet** | 51,300 | Largest 3D model repository | Chang et al., 2015 |
| **OmniObject3D** | 6,000 | 190 categories, real-scanned | Wu et al., 2023 |

### 6D Pose Estimation

| Dataset | Objects | Key Feature | Citation |
|---------|--------:|-------------|----------|
| **KITchen** | 111 | Humanoid egocentric, 205K RGB-D | Younes & Asfour, 2024 |
| **HOPE** | 28 | BOP-compatible, grocery items | Tyree et al., 2022 |
| **BOP** | multi | Unified 6D pose benchmark | Hodaň et al., 2018 |
| **T-LESS** | 30 | Texture-less industrial objects | Hodaň et al., 2017 |

### Grasp & Manipulation

| Dataset | Key Feature | Citation |
|---------|-------------|----------|
| **GraspNet-1Billion** | 88 objects, 1.1B grasp poses | Fang et al., 2020 |
| **DexYCB** | Hand-object grasping, 20 YCB objects | Chao et al., 2021 |
| **ACRONYM** | 8,872 objects, 17.7M grasp labels | Eppner et al., 2021 |
| **ContactDB** | Thermal grasp contact maps | Brahmbhatt et al., 2019 |
| **Dex-Net** | Grasp quality CNN, synthetic depth | Mahler et al., 2017 |

### 2D Detection & Segmentation

| Dataset | Key Feature | Citation |
|---------|-------------|----------|
| **Open Images V7** | 9M images, 600 classes, 16M bboxes | Kuznetsova et al., 2020 |
| **OCID** | Indoor clutter, tabletop segmentation | Suchi et al., 2019 |

### Articulated Objects

| Dataset | Key Feature | Citation |
|---------|-------------|----------|
| **AKB-48** | 2,037 articulated objects (drawers, doors) | Liu et al., 2022 |

---

## YCB Mapping

**30 of our 100 objects** have direct YCB counterparts with available 3D models:

```
024_bowl        → bowl           (exact)
025_mug         → cup            (exact)
029_plate       → plate          (exact)
030_fork        → fork           (exact)
031_spoon       → spoon          (exact)
013_apple       → apple          (exact)
011_banana      → banana         (exact)
014_lemon       → lemon          (exact)
006_mustard     → mustard        (exact)
007_tuna_fish   → tuna_can       (exact)
077_rubiks_cube → rubiks_cube    (exact)
...
```

Full mapping: `object/sources/ycb_mapping.yaml`

---

## Competition History

Objects were curated from **3 years** of RoboCup@Home competitions:

| Year | Location | Notable Local Objects |
|------|----------|---------------------|
| 2025 | Salvador :flag_br: | kuat, corn_flour, broth |
| 2024 | Eindhoven :flag_nl: | stroopwafel, dubbelfris, hagelslag |
| 2023 | Bordeaux :flag_fr: | red_wine, tropical_juice |

---

## File Structure

```
object/
├── README.md                          # Overview & usage
├── taxonomy.yaml                      # 100 objects with full metadata
├── sources/
│   ├── citations.bib                  # 18 datasets, BibTeX
│   ├── dataset_sources.yaml           # Dataset registry with URLs
│   ├── ycb_mapping.yaml               # YCB ↔ taxonomy mapping
│   └── kitchen_mapping.yaml           # KITchen ↔ taxonomy mapping
└── categories/
    ├── dishes.yaml
    ├── drinks.yaml
    ├── fruits.yaml
    ├── snacks.yaml
    ├── foods.yaml
    ├── cleaning_supplies.yaml
    └── toys.yaml
```

---

## Citation

```bibtex
@misc{inharby1dataset2026,
  title  = {{INHA-RBY1} Object Taxonomy for {RoboCup@Home} Service Robots},
  author = {{Inha-United}},
  year   = {2026},
  url    = {https://github.com/inha-united-athome/inha-rby1-dataset}
}
```
