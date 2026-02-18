# ConcisePPG
Concise PPG Features for lightweight Identity Verification

If you use this work in your research, please cite it as follows:
```bash
Shahmirzadi, D., Wang, W.F. Concise PPG features for lightweight identity verification. Multimed Tools Appl 85, 147 (2026). https://doi.org/10.1007/s11042-026-21295-6
```
Here is the link to [Springer Nature](https://link.springer.com/article/10.1007/s11042-026-21295-6)

I’m pleased to share a full-text, view-only version of my latest paper via Springer Nature’s SharedIt initiative: [[Link](https://rdcu.be/e2FpX)]


# 📈 PPG-Based Lightweight Identity Verification Using a Single Cardiac Cycle

This repository contains the full implementation of our paper:  
**"Concise PPG Features for Lightweight Identity Verification Using a Single Cardiac Cycle"**

> 📝 Manuscript submitted to [journal/conference name], 2025.

---

## 🔍 Overview

This project presents a lightweight, efficient, and high-accuracy biometric verification system based on **photoplethysmography (PPG)** signals. Unlike previous approaches that require long or multiple cycles of data, our method achieves **99.96% accuracy using only a single cardiac cycle**, making it ideal for embedded and resource-constrained environments like wearables and IoT devices.

### 🚀 Key Contributions
- **Single cardiac cycle** authentication
- **Custom HF HRV feature** for enhanced accuracy
- **DTW-based normalization** and advanced preprocessing
- **Runtime benchmarks** on both PC and Raspberry Pi
- Achieves **real-time feasibility** for portable biometric systems

---


---

## 🧠 Methodology

The pipeline includes:
1. **Bandpass Filtering** using DB4 wavelet and Butterworth filters.
2. **Cardiac Cycle Segmentation** via peak and foot detection.
3. **Outlier Removal** based on RR interval thresholds.
4. **Normalization** of each cycle to 150 samples using DTW.
5. **Feature Extraction** including handcrafted HF HRV.
6. **Classification** using Gradient Boost, SVM, and other models.

---

## 📊 Runtime Benchmarks

We benchmarked the execution time of each component on both a desktop PC and a **Raspberry Pi 4 (8 GB RAM)**:

| Task                   | PC (s)   | Raspberry Pi (s) |
|------------------------|----------|------------------|
| Feature Extraction     | 0.0001   | 0.030            |
| Segmentation           | 0.0030   | 0.101            |
| DTW Transformation     | 2.0858   | 3.548            |

These results confirm the pipeline's viability for embedded systems and real-time execution.

---

## 📁 Dataset

The code is built for the **BioSec2 PPG dataset**, collected at the University of Toronto BioSec.Lab under ethical protocol #33788 [28]. The dataset includes:
- 100 participants (48 male, 52 female)
- 2 sessions × 3 trials × ~90 seconds
- Sensor: Plux reflective PPG, 100 Hz sampling
- Available upon request for academic use

🔐 *Due to privacy constraints, the dataset is not included here. Please contact the authors or BioSec.Lab to obtain access.*

---

## 🛠 Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

▶️ Running the Code

```bash
python benchmark.py
```


