# csv-driven-image-transformation
A two-stage image alignment pipeline that automates batch image transformations using CSV-based parameters. The first phase allows manual parameter tuning and CSV generation, while the second phase performs automated alignment and transformation of multiple TIFF images using OpenCV and tifffile.

# 🧠 Image Alignment Automation Pipeline

This repository implements a **two-phase image transformation and alignment workflow** designed to automate batch processing of TIFF images using **CSV-based transformation parameters**.

---

## ⚙️ Overview

The pipeline is divided into two main parts:

### 1️⃣ Manual Transformation Phase
- Transformation parameters (rotation, scale, offset, warp values, etc.) are determined manually or semi-automatically.
- The calculated parameters are saved into a **CSV file** (e.g., `V3_transform.csv`).
- This CSV acts as a reusable configuration that defines the transformation for future use.

### 2️⃣ Automated Batch Processing Phase
- The second script automatically reads the parameters from the CSV.
- It applies the same transformation to a **batch of TIFF images** in the selected folders.
- Output images are saved in a newly created `_transformed` folder.

---

## 🧩 Features

- Supports **any common image format** (TIFF, PNG, JPEG, BMP, etc.)
- Performs **rotation, scaling, translation, and perspective warping**.
- Reads **transformation parameters from CSV** for automation.
- Uses **Tkinter GUI** for folder selection.
- Saves all transformed images in a dedicated output folder.
- Automatically matches images by filename pattern (last 3 characters).

---

## 🧰 Requirements

Install the following Python packages before running:

```bash
pip install opencv-python numpy pandas tifffile imagecodecs
