# 🌀 YOLOv8-CBAM for Wind Turbine Blade Defect Segmentation

This repository contains a custom semantic segmentation model based on **YOLOv8**, enhanced with **Convolutional Block Attention Modules (CBAM)**, designed for the detection of small structural defects in wind turbine blade crops.

## 🔍 Overview

Structural defects in wind turbine blades can compromise efficiency and safety. This project proposes a lightweight segmentation model capable of detecting small and sparse defects in binary form (defect vs. background) using attention-aware feature extraction.

## 🧠 Architecture

- Backbone: YOLOv8-inspired with CBAM in each C2f block
- Head: Lightweight transposed convolution for segmentation
- Attention: Channel + Spatial attention via CBAM
- Input: 256×256 cropped patches from Blade30 dataset

<p align="center">
  <img src="images/architecture_diagram.png" width="600"/>
</p>

## 📂 Dataset

The model is trained on the [Blade30 Dataset](https://doi.org/10.21227/h1sw-8h48), using:
- **Cropped RGB images (256x256)** containing defect regions.
- **Binary PNG masks** with 1 = defect, 0 = background.

Example input crops:

<p align="center">
  <img src="images/blade30_ex_images_crops.png" width="500"/>
</p>

## 🏗️ Installation

```bash
git clone https://github.com/your-username/yolov8-cbam-blade-defect.git
cd yolov8-cbam-blade-defect
pip install -r requirements.txt
