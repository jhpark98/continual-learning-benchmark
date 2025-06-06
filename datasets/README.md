Please download the datasets from this [google drive link](https://drive.google.com/file/d/1e2f0DsZpf-brsjwrvY99TrutN-aOl2ym/view?usp=sharing) and place them in this directory.

# Continual Learning Benchmark: Human Activity Recognition Datasets

This repository reproduces the experiments in the [Continual Learning Benchmark](https://github.com/srvCodes/continual-learning-benchmark) focused on micro-F1 performance for human activity recognition using real-world wearable sensor datasets.

> ⚠️ Note: The original Google Drive link to the datasets is broken. This README provides alternative verified sources to obtain the datasets individually.

---

## 📋 Table of Contents

- [Datasets](#datasets)
  - [1. PAMAP2](#1-pamap2)
  - [2. DSADS](#2-dsads)
  - [3. HAPT](#3-hapt)
  - [4. UCI HAR](#4-uci-har)
  - [5. WISDM](#5-wisdm)
  - [6. Skoda Mini Checkpoint](#6-skoda-mini-checkpoint)
  - [7. USC-HAD](#7-usc-had)
  - [8. Opportunity](#8-opportunity)
- [Data Preprocessing](#data-preprocessing)
- [Citation](#citation)

---

## 📂 Datasets

Below are the eight datasets used in the benchmark, along with a short summary and download link.

### 1. PAMAP2
- **Summary**: Includes IMU and heart rate data for 18 physical activities.
- **Download**: [UCI PAMAP2 Dataset](https://archive.ics.uci.edu/ml/datasets/pamap2+physical+activity+monitoring)

---

### 2. DSADS (Daily and Sports Activities Dataset)
- **Summary**: Contains 19 activities by 8 subjects using 5 body-worn sensors.
- **Download**: [DSADS Dataset](https://archive.ics.uci.edu/ml/datasets/daily+and+sports+activities)

---

### 3. HAPT (Human Activities and Postural Transitions)
- **Summary**: Extension of the UCI HAR dataset, includes transitions and more fine-grained labels.
- **Download**: [HAPT Dataset](https://archive.ics.uci.edu/ml/datasets/Human+Activities+and+Postural+Transitions)

---

### 4. UCI HAR (Human Activity Recognition Using Smartphones)
- **Summary**: Smartphone accelerometer and gyroscope data for 6 activities by 30 individuals.
- **Download**: [UCI HAR Dataset](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones)

---

### 5. WISDM
- **Summary**: Accelerometer data from smartphones and smartwatches for common activities.
- **Download**: [WISDM Dataset](http://www.cis.fordham.edu/wisdm/dataset.php)

---

### 6. Skoda Mini Checkpoint
- **Summary**: Assembly-line worker activity data from arm-mounted sensors.
- **Download**: [Skoda Dataset](https://archive.ics.uci.edu/ml/datasets/Skoda+Mini+Check+Point)

---

### 7. USC-HAD (USC Human Activity Dataset)
- **Summary**: 12 activity types recorded from 14 subjects using motion sensors.
- **Download**: [USC-HAD Dataset](https://sipi.usc.edu/had/)

---

### 8. Opportunity Activity Recognition
- **Summary**: Multimodal wearable sensor data in a smart home setup with rich activity labels.
- **Download**: [Opportunity Dataset](https://archive.ics.uci.edu/ml/datasets/opportunity+activity+recognition)

---

## ⚙️ Data Preprocessing

To prepare the datasets:

1. Download all datasets into a common folder structure (e.g., `./datasets/`).
2. Use the scripts provided in `utils/data_handler.py` and `utils/join_pickles.py` from the [original repository](https://github.com/srvCodes/continual-learning-benchmark) to:
   - Clean and normalize time-series data
   - Align sampling rates
   - Export `.pkl` files for each dataset and task
