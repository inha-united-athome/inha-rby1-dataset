<div align="center">
  <img src="https://github.com/inha-united-athome/.github/raw/main/profile/inha_logo.png" width="110" /><br/>
  <h1>📁 inha-rby1-dataset</h1>
  <span><b>Inha-United real-world RB-Y1 humanoid demonstration dataset for diverse manipulation tasks.</span><br/><br/>
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
</div>

<p align="center">
  <img src="assets/thumbnail.png" width="90%" style="display:block; margin:0 auto;"/>
</p>

## Dataset Overview
The **INHA-RBY1 Dataset** is a real-world humanoid manipulation dataset collected with the Rainbow Robotics RB-Y1 platform, covering a diverse set of manipulation tasks.

<table align="center" width="90%">
  <tr>
    <td align="center">
      <img src="assets/pick_basket.gif" width="100%">
    </td>
    <td align="center">
      <img src="assets/pick_banana.gif" width="100%">
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="assets/pour_sprite.gif" width="100%">
    </td>
    <td align="center">
      <img src="assets/open_washer.gif" width="100%">
    </td>
  </tr>
</table>

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