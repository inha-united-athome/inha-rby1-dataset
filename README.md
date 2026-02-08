# 📁 inha-rby1-dataset

<p align="center">
  <a href="https://inha-united.github.io/Home2026/">
    <img src="https://img.shields.io/badge/Website-INHA--UNITED-black.svg" alt="Website">
  </a>
  <a href="https://www.youtube.com/@Inha-United_Home">
    <img src="https://img.shields.io/badge/YouTube-INHA--UNITED-red.svg?logo=youtube&logoColor=white" alt="YouTube">
  </a>
  <a href="https://inha-united-athome.github.io/inha-rby1-dataset/">
    <img src="https://img.shields.io/badge/Docs-v0.1-blue.svg" alt="Documentation">
  </a>
  <a href="https://huggingface.co/inha-united-athome">
    <img src="https://img.shields.io/badge/🤗-HuggingFace-yellow.svg" alt="Hugging Face">
  </a>
  <a href="https://www.rainbow-robotics.com">
    <img src="https://img.shields.io/badge/RainbowRobotics-Official-6f42c1.svg">
  </a>
</p>

Inha-United real-world RB-Y1 humanoid demonstration dataset for diverse manipulation tasks.
<p align="center">
  <img src="assets/thumbnail.png" width="90%" style="display:block; margin:0 auto;"/>
</p>

---

## Dataset Overview
The **INHA-RBY1 Dataset** is a real-world humanoid manipulation dataset collected with the Rainbow Robotics RB-Y1 platform, covering a diverse set of manipulation tasks.

<div style="width:90%; margin:0 auto; display:flex; flex-wrap:wrap; gap:6px;">
  <img src="assets/pick_basket.gif" style="width:calc(50% - 3px); display:block;"/>
  <img src="assets/pick_banana.gif" style="width:calc(50% - 3px); display:block;"/>
  <img src="assets/pour_sprite.gif" style="width:calc(50% - 3px); display:block;"/>
  <img src="assets/open_washer.gif" style="width:calc(50% - 3px); display:block;"/>
</div>

## File Structure
```
    rby1-datasets
        └── rby1_YYYYMMDD_HHMMS/
            ├── data/               # Parquet data
            ├── videos/             # Video files
            ├── frames/             # Cached keyframes
            ├── annotations/        # Human-labeled data
            └── meta/               # Metadata   
```

## Documentation
For more details on the data collection process, dataset structure, download links, and usage examples, please visit our documentation page.

<p align="center">
  <a href="https://inha-united-athome.github.io/inha-rby1-dataset/">
    <strong style="font-size: 1.6em;">👉 INHA-RBY1-Dataset Documentation Page</strong>
  </a>
</p>

## License
Copyright &copy; 2026 Inha-United