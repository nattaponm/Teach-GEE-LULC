# Teach-GEE-LULC

## Teaching Land Use / Land Cover Classification with Google Earth Engine Python API

**Sentinel-2 Optical Remote Sensing · Sentinel-1 SAR · Random Forest · Accuracy Assessment · Multitemporal Analysis · Data Fusion**

[![GitHub](https://img.shields.io/badge/GitHub-Teach--GEE--LULC-181717?logo=github)](https://github.com/nattaponm/Teach-GEE-LULC)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/01_Sentinel2_Point_LULC_Classification.ipynb)
[![YouTube Playlist](https://img.shields.io/badge/YouTube-Teaching%20Playlist-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/playlist?list=PL2e-NEAjUyLEThjWtOqUyVtzBZcIm_Ha4)
[![Google Earth Engine](https://img.shields.io/badge/Google-Earth%20Engine-4285F4?logo=googleearthengine&logoColor=white)](https://developers.google.com/earth-engine)
[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Sentinel-2](https://img.shields.io/badge/Data-Sentinel--2-2E8B57)](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)
[![Sentinel-1](https://img.shields.io/badge/Data-Sentinel--1-4169E1)](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S1_GRD)

---

## About this repository

Repository นี้จัดทำขึ้นเพื่อใช้เป็นสื่อการเรียนการสอนด้าน **Remote Sensing, Geoinformatics, Environmental Science และ Land Use / Land Cover (LULC) Classification** โดยใช้ **Google Earth Engine (GEE) Python API** บน **Google Colab** เป็นแพลตฟอร์มหลัก

พื้นที่ตัวอย่างคือ **พิษณุโลก ประเทศไทย** โดยใช้ Sentinel-2 และ Sentinel-1 เพื่อให้ผู้เรียนค่อย ๆ พัฒนาความเข้าใจจากการอ่านภาพดาวเทียม การออกแบบ training samples การจำแนกด้วย Random Forest การประเมินความถูกต้อง การวิเคราะห์ SAR หลายช่วงเวลา และการรวมข้อมูล Optical + SAR

หลักการสำคัญของชุดการสอนนี้คือ

> **Readable code > compact code**  
> **One code cell = one concept**  
> **Scientific interpretation > running code without understanding**

เป้าหมายจึงไม่ใช่เพียง “รันโค้ดให้ได้ผลลัพธ์” แต่ต้องเข้าใจว่า **sensor วัดอะไร, predictor มีความหมายอย่างไร, reference samples ถูกสร้างอย่างไร, model เรียนรู้อะไร และผลลัพธ์มีข้อจำกัดอะไร**

---

# Teaching origin and code development

แนวคิดการเรียนการสอนและตัวอย่างโค้ดใน repository นี้ **พัฒนาและดัดแปลงต่อยอดจากชุดวิดีโอการสอนด้าน Google Earth Engine, Remote Sensing และ Geospatial Analysis ของ รศ.ดร.นัฐพล มหาวิค**  
สาขาวิทยาศาสตร์สิ่งแวดล้อม คณะเกษตรศาสตร์ ทรัพยากรธรรมชาติและสิ่งแวดล้อม มหาวิทยาลัยนเรศวร

Notebook ชุดนี้ได้นำแนวคิดจากสื่อการสอนเดิมมาปรับโครงสร้างใหม่ให้อยู่ในรูปแบบ

```text
YouTube teaching concepts
        ↓
Google Earth Engine Python API
        ↓
Google Colab notebooks
        ↓
Interactive Folium maps
        ↓
Training-sample design
        ↓
Accuracy assessment
        ↓
Sentinel-1 SAR multitemporal analysis
        ↓
Sentinel-1 + Sentinel-2 data fusion
        ↓
GeoTIFF / CSV outputs for GIS analysis
```

▶️ **YouTube Teaching Playlist**  
https://www.youtube.com/playlist?list=PL2e-NEAjUyLEThjWtOqUyVtzBZcIm_Ha4

> **YouTube explains the concepts; GitHub organizes the workflow; Colab lets students reproduce the analysis.**  
> **YouTube ใช้อธิบายแนวคิด GitHub ใช้จัดระบบบทเรียน และ Google Colab ใช้ทดลองและทำซ้ำการวิเคราะห์ด้วยตนเอง**

---

# Course philosophy

แนวทางการเรียนรู้ของ repository นี้คือ

$$ \text{Observe} \rightarrow \text{Interpret} \rightarrow \text{Sample} \rightarrow \text{Classify} \rightarrow \text{Validate} \rightarrow \text{Compare} \rightarrow \text{Explain} $$

### Observe
ดูข้อมูลดาวเทียมและ spatial pattern ก่อนเริ่มคำนวณ

### Interpret
เข้าใจความหมายทางกายภาพของ spectral reflectance และ radar backscatter

### Sample
ออกแบบและตรวจคุณภาพ reference / training samples รวมถึง spatial support

### Classify
ใช้ machine learning เพื่อเรียนรู้ความสัมพันธ์ระหว่าง predictors และ land-cover classes

### Validate
ใช้ hold-out validation data ที่ไม่ได้นำไป train model

### Compare
เปรียบเทียบ sampling designs, sensors, temporal information และ fusion strategies

### Explain
อธิบายผลลัพธ์ด้วยหลัก Remote Sensing และ GIS ไม่ใช่เพียงดูค่า accuracy

---

# Learning pathway

แนะนำให้เรียนตามลำดับ

```text
01 Sentinel-2 Point Classification
              ↓
02 Sentinel-2 Rectangle Classification
              ↓
03 Sentinel-1 SAR Fundamentals
              ↓
04 Sentinel-1 Multitemporal Classification
              ↓
05 Sentinel-1 + Sentinel-2 Data Fusion
```

แต่ละ Notebook ถูกออกแบบให้ **รันได้แบบ standalone** ขณะที่แนวคิดการเรียนต่อเนื่องจากบทก่อนหน้า

---

# Notebook overview

| No. | Notebook | Main question | GitHub | Colab |
|---|---|---|---|---|
| 01 | Sentinel-2 Point LULC Classification | จุดตัวอย่างสามารถใช้จำแนก LULC ได้อย่างไร? | [View](01_Sentinel2_Point_LULC_Classification.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/01_Sentinel2_Point_LULC_Classification.ipynb) |
| 02 | Sentinel-2 Rectangle LULC Classification | Spatial support ของ training sample มีผลอย่างไร? | [View](02_Sentinel2_Rectangle_LULC_Classification.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/02_Sentinel2_Rectangle_LULC_Classification.ipynb) |
| 03 | Sentinel-1 SAR Fundamentals | SAR วัดอะไร และอ่าน VV/VH อย่างไร? | [View](03_Sentinel1_SAR_Fundamentals.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/03_Sentinel1_SAR_Fundamentals.ipynb) |
| 04 | Sentinel-1 Multitemporal LULC Classification | Temporal SAR ช่วย classification หรือไม่? | [View](04_Sentinel1_Multitemporal_LULC_Classification.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/04_Sentinel1_Multitemporal_LULC_Classification.ipynb) |
| 05 | Sentinel-1 + Sentinel-2 Data Fusion | Optical และ SAR ให้ข้อมูลเสริมกันหรือไม่? | [View](05_Sentinel1_Sentinel2_Data_Fusion.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/05_Sentinel1_Sentinel2_Data_Fusion.ipynb) |

---

# Quick start

1. ลงชื่อเข้าใช้ Google account
2. ลงทะเบียนใช้งาน Google Earth Engine
3. เปิด Notebook 01 ด้วยปุ่ม **Open in Colab**
4. กำหนด Google Cloud Project ของตนเอง

```python
PROJECT = "YOUR_GOOGLE_CLOUD_PROJECT_ID"
```

5. Authenticate และ Initialize Earth Engine
6. รัน Notebook ตามลำดับ 01 → 05

> Public notebooks ไม่ควรใช้ Google Cloud Project ID ส่วนบุคคลของผู้สอน

---

# Module 01 — Sentinel-2 Point LULC Classification

[View on GitHub](01_Sentinel2_Point_LULC_Classification.ipynb) · [Open in Colab](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/01_Sentinel2_Point_LULC_Classification.ipynb)

## What you will learn

- Sentinel-2 Surface Reflectance คืออะไร
- spectral bands แต่ละช่วงตอบสนองกับ land cover อย่างไร
- NDVI, NDWI และ NDBI คืออะไร
- reference points ถูกใช้เป็น training samples อย่างไร
- Random Forest ทำงานในระดับแนวคิดอย่างไร
- confusion matrix และ accuracy metrics อ่านอย่างไร
- training accuracy ต่างจาก validation accuracy อย่างไร

## Key concepts

```text
Spectral reflectance
Cloud masking
Spectral indices
Feature vector
Training / validation split
Random Forest
Confusion matrix
OA / PA / UA / F1
```

## Key equations

### Surface reflectance scaling

$$ \rho = DN \times 10^{-4} $$

### NDVI

$$ NDVI = \frac{B8-B4}{B8+B4} $$

### NDWI

$$ NDWI = \frac{B3-B8}{B3+B8} $$

### NDBI

$$ NDBI = \frac{B11-B8}{B11+B8} $$

NDVI ไม่ใช่ Forest class, NDWI ไม่ใช่ Water class และ NDBI ไม่ใช่ Urban class โดยอัตโนมัติ  
indices เหล่านี้เป็น **predictor variables**

### Sentinel-2 feature vector

$$ \mathbf{x}_{S2} = [ B2,B3,B4,B8,B11,B12, NDVI,NDWI,NDBI ] $$

### Random Forest

ถ้ามี decision trees จำนวน $B$ ต้น

$$ \hat{y} = \operatorname{mode} \left[ h_1(\mathbf{x}), h_2(\mathbf{x}), \dots, h_B(\mathbf{x}) \right] $$

### Confusion matrix

ให้ $n_{ij}$ เป็นจำนวน reference samples ของ class $i$ ที่ถูกจำแนกเป็น class $j$

- Rows = reference / actual classes
- Columns = predicted classes

### Overall Accuracy

$$ OA = \frac{\sum_i n_{ii}}{N} $$

### Producer's Accuracy

$$ PA_i = \frac{n_{ii}} {\sum_j n_{ij}} $$

### User's Accuracy

$$ UA_i = \frac{n_{ii}} {\sum_j n_{ji}} $$

### F1 score

$$ F1_i = \frac{2(PA_i)(UA_i)} {PA_i+UA_i} $$

## What you will produce

```text
Sentinel-2 composite
Spectral-index layers
Point-trained Random Forest model
Confusion matrix
Class-specific accuracy metrics
LULC GeoTIFF
```

---

# Module 02 — Sentinel-2 Rectangle Training

[View on GitHub](02_Sentinel2_Rectangle_LULC_Classification.ipynb) · [Open in Colab](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/02_Sentinel2_Rectangle_LULC_Classification.ipynb)

## What you will learn

- spatial support คืออะไร
- point และ rectangle training ต่างกันอย่างไร
- training location และ training pixel ต่างกันอย่างไร
- mixed pixel คืออะไร
- edge effect คืออะไร
- ทำไม training pixels มากขึ้นไม่ได้แปลว่า independent samples มากขึ้น
- เปรียบเทียบ Point vs Rectangle โดยควบคุมตัวแปรอื่นให้เหมือนกัน

## Key concepts

```text
Spatial support
Training geometry
Mixed pixel
Edge effect
Spatial dependence
Controlled experiment
```

## Key equations

### Training-window area

$$ A_{window}=w\times h $$

สำหรับ 20 × 20 m:

$$ A_{window}=400~m^2 $$

สำหรับ Sentinel-2 10-m pixel:

$$ A_{pixel}\approx100~m^2 $$

จำนวน output-grid pixels โดยประมาณ:

$$ n \approx \frac{A_{window}} {A_{pixel}} $$

### Mixed pixel

$$ R_{pixel} \approx \sum_{k=1}^{K} f_kR_k $$

โดย

$$ \sum_{k=1}^{K}f_k=1 $$

### Independent sampling concept

$$ n_{pixels} \neq n_{independent\ locations} $$

> **Training quantity ≠ Training quality**

## What you will produce

```text
20 × 20 m training rectangles
Training-pixel counts by class
Point vs Rectangle comparison
Class-specific F1 comparison
Rectangle-based LULC GeoTIFF
```

---

# Module 03 — Sentinel-1 SAR Fundamentals

[View on GitHub](03_Sentinel1_SAR_Fundamentals.ipynb) · [Open in Colab](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/03_Sentinel1_SAR_Fundamentals.ipynb)

## What you will learn

- Active vs passive remote sensing
- C-band SAR คืออะไร
- VV และ VH คืออะไร
- radar backscatter หมายถึงอะไร
- dB scale อ่านอย่างไร
- smooth-surface, rough-surface, volume และ double-bounce scattering
- speckle คืออะไร
- orbit geometry และ incidence angle สำคัญอย่างไร
- monthly temporal signatures คืออะไร

## Key concepts

```text
Active sensing
Radar backscatter
VV / VH polarization
Decibel
Scattering mechanisms
Speckle
Orbit geometry
Incidence angle
Temporal signature
```

## Key equations

### Backscatter in decibels

$$ \sigma^0_{dB} = 10\log_{10} \left( \sigma^0_{linear} \right) $$

### Back to linear domain

$$ \sigma^0_{linear} = 10^{\sigma^0_{dB}/10} $$

ดังนั้น -10 dB มี backscatter สูงกว่า -20 dB

### Polarization contrast

$$ D_{VV-VH} = VV_{dB}-VH_{dB} $$

ซึ่งสัมพันธ์กับ linear ratio:

$$ VV_{dB}-VH_{dB} = 10\log_{10} \left( \frac{VV_{linear}} {VH_{linear}} \right) $$

### Conceptual radar response

$$ \sigma^0 = f( \text{roughness}, \text{moisture}, \text{structure}, \theta_i, \text{geometry}, \dots ) $$

### Monthly class signature

สำหรับ class $c$ และเดือน $m$

$$ \tilde{\sigma}^{0}_{c,m} = \operatorname{median} \left( \sigma^{0}_{i,m} \right) $$

### Annual SAR feature vector

$$ \mathbf{x}_{S1} = [ VV_{Jan},VH_{Jan}, \dots, VV_{Dec},VH_{Dec} ] $$

$$ p=24 $$

## What you will produce

```text
VV maps
VH maps
VV − VH polarization contrast
Single-scene vs monthly-median comparison
Monthly VV temporal profiles
Monthly VH temporal profiles
24-band Sentinel-1 temporal stack
```

---

# Module 04 — Sentinel-1 Multitemporal Classification

[View on GitHub](04_Sentinel1_Multitemporal_LULC_Classification.ipynb) · [Open in Colab](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/04_Sentinel1_Multitemporal_LULC_Classification.ipynb)

## What you will learn

- GRD asset count ต่างจาก independent acquisition dates อย่างไร
- ทำไม same-date frames ควรถูก mosaic ก่อน monthly composite
- single-period SAR ต่างจาก annual multitemporal SAR อย่างไร
- temporal information ช่วย class ใด
- Random Forest variable importance อ่านอย่างไร
- correlated predictors มีผลต่อ importance อย่างไร
- temporal-label consistency คืออะไร

## Experiment design

```text
Model A
January SAR
2 predictors

vs

Model B
January–December SAR
24 predictors
```

## Key equations

### January baseline

$$ \mathbf{x}^{Jan} = [ VV_{Jan}, VH_{Jan} ] $$

$$ p=2 $$

### Annual multitemporal SAR

$$ \mathbf{x}^{Annual} = [ VV_{Jan},VH_{Jan}, \dots, VV_{Dec},VH_{Dec} ] $$

$$ p=24 $$

### Change in Overall Accuracy

$$ \Delta OA = OA_{Annual} - OA_{Jan} $$

### Class-specific change

$$ \Delta F1_i = F1_{Annual,i} - F1_{Jan,i} $$

### Normalized variable importance

$$ I_j^* = \frac{I_j} {\sum_{k=1}^{p}I_k} $$

### Importance aggregated by month

$$ I_m = I_{VV_m} + I_{VH_m} $$

> **Variable importance does not imply causation.**

## What you will produce

```text
January SAR classification
Annual SAR classification
OA / Mean F1 comparison
Class-specific F1 comparison
Monthly variable importance
VV vs VH importance
GeoTIFF outputs
```

---

# Module 05 — Sentinel-1 + Sentinel-2 Data Fusion

[View on GitHub](05_Sentinel1_Sentinel2_Data_Fusion.ipynb) · [Open in Colab](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/05_Sentinel1_Sentinel2_Data_Fusion.ipynb)

## What you will learn

- mapping area ต่างจาก reference-data domain อย่างไร
- feature-level fusion คืออะไร
- optical กับ SAR complement กันอย่างไร
- common validation support คืออะไร
- same-period fusion ต่างจาก annual fusion อย่างไร
- sensor-level variable importance
- spatial disagreement map
- ทำไม more predictors ไม่ได้แปลว่า better model

## Experiment design

| Model | Information | Predictors |
|---|---|---:|
| A | Sentinel-2 January | 9 |
| B | Sentinel-1 January | 2 |
| C | Sentinel-2 + Sentinel-1 January | 11 |
| D | Sentinel-2 + Annual Sentinel-1 | 33 |

## Key equations

### Sentinel-2 feature space

$$ \mathbf{x}_{S2}\in\mathbb{R}^{9} $$

### January Sentinel-1 feature space

$$ \mathbf{x}_{S1,Jan}\in\mathbb{R}^{2} $$

### Same-period fusion

$$ \mathbf{x}_{Fusion,Jan} = [ \mathbf{x}_{S2}, \mathbf{x}_{S1,Jan} ] $$

$$ p=11 $$

### Optical + annual SAR fusion

$$ \mathbf{x}_{Fusion,Annual} = [ \mathbf{x}_{S2}, \mathbf{x}_{S1,Annual} ] $$

$$ p=33 $$

### Common valid-data support

$$ M_{common} = M_{S2} \cap M_{S1} $$

### Sensor-level importance

$$ I_{S2} = \sum_{j\in S2} I_j^* $$

$$ I_{S1} = \sum_{j\in S1} I_j^* $$

### Spatial disagreement

$$ D(x) = \begin{cases} 0, & C_A(x)=C_B(x) \\ 1, & C_A(x)\neq C_B(x) \end{cases} $$

> **Disagreement does not automatically mean error.**

> **More predictors do not automatically produce a better model.**

## What you will produce

```text
Sentinel-2-only classification
Sentinel-1-only classification
Same-period S1 + S2 fusion
Annual-SAR fusion
Model comparison table
Class-specific F1 comparison
Sensor-level variable importance
Spatial disagreement map
Final fusion GeoTIFF
```

---

# Example teaching results

ผลต่อไปนี้เป็น **ตัวอย่างจาก reference dataset และ hold-out samples ในชุดการสอนนี้เท่านั้น** ไม่ควรตีความเป็น publication-grade regional accuracy assessment

| Model | Predictors | Overall Accuracy | Mean F1 |
|---|---:|---:|---:|
| Sentinel-2 January | 9 | 93.3% | 0.933 |
| Sentinel-1 January | 2 | 70.0% | 0.686 |
| Sentinel-2 + Sentinel-1 January | 11 | **96.7%** | **0.966** |
| Sentinel-2 + Annual Sentinel-1 | 33 | 93.3% | 0.931 |

same-period optical–SAR fusion ให้ผลดีที่สุดใน hold-out sample ชุดนี้ ขณะที่การเพิ่ม temporal predictors จำนวนมากไม่ได้ทำให้ accuracy สูงขึ้นเสมอ

Validation set มี 30 จุด ดังนั้น validation point หนึ่งจุดคิดเป็น

$$ \frac{1}{30}\times100 = 3.33\% $$

ของ Overall Accuracy

จึงควรระวังการตีความความแตกต่างระหว่าง 93.3% และ 96.7% ว่าเป็น superiority ที่แน่นอน

---

# Scientific interpretation rules

- **NDVI ≠ Forest class**
- **NDWI ≠ Water class**
- **NDBI ≠ Urban class**
- **Training pixels ≠ independent reference locations**
- **Training accuracy ≠ map accuracy**
- **Variable importance ≠ causation**
- **Map disagreement ≠ error**
- **More predictors ≠ better model**
- **High accuracy ≠ perfect class definition**
- **Mapping extent ≠ reference-data extent**

---

# Core tools and libraries

[![Earth Engine](https://img.shields.io/badge/Google-Earth%20Engine-Python%20API-4285F4?logo=googleearthengine&logoColor=white)](https://developers.google.com/earth-engine/guides/python_install)
[![Google Colab](https://img.shields.io/badge/Google-Colab-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/)
[![Folium](https://img.shields.io/badge/Library-Folium-77B829)](https://python-visualization.github.io/folium/)
[![Pandas](https://img.shields.io/badge/Library-pandas-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/Library-NumPy-013243?logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-11557C)](https://matplotlib.org/)

```python
import ee
import folium
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

Random Forest ใช้ `ee.Classifier.smileRandomForest()` ของ Google Earth Engine

---

# Earth Engine datasets

### Sentinel-2 Surface Reflectance Harmonized

[`COPERNICUS/S2_SR_HARMONIZED`](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)

ใช้สำหรับ visible, NIR, SWIR, spectral indices และ optical LULC classification

### Sentinel-1 GRD

[`COPERNICUS/S1_GRD`](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S1_GRD)

ใช้สำหรับ VV/VH backscatter, SAR interpretation, multitemporal analysis และ optical–SAR fusion

### Administrative boundary

[`FAO/GAUL/2025/level2`](https://developers.google.com/earth-engine/datasets/catalog/FAO_GAUL_2025_level2)

ใช้กำหนดพื้นที่แสดงผลระดับอำเภอ

---

# Reference data

ไฟล์ reference samples:

```text
data/phitsanulok_lulc_points.csv
```

| Class ID | Class |
|---:|---|
| 0 | Urban / Built-up |
| 1 | Water |
| 2 | Forest / Tree cover |
| 3 | Agriculture |
| 4 | Bare soil / Open land |

ชุดข้อมูลนี้มีไว้สำหรับ **teaching and methodological demonstration** ไม่ใช่ probability-based regional accuracy assessment

---

# Outputs

Notebooks สามารถ export ผลลัพธ์ไป Google Drive เพื่อใช้ต่อใน QGIS หรือ GIS software อื่น

```text
PHS_S2_Point_RF_LULC_2021.tif
PHS_S2_Rectangle_RF_LULC_2021.tif
PHS_S1_January_RF_LULC_2021.tif
PHS_S1_Annual_RF_LULC_2021.tif
PHS_S2_S1_Annual_Fusion_RF_LULC_2021.tif
```

โดยทั่วไปใช้

```text
CRS    = EPSG:32647
Scale  = 10 m
NoData = 255
```

---

# Repository structure

```text
Teach-GEE-LULC/
│
├── README.md
│
├── 01_Sentinel2_Point_LULC_Classification.ipynb
├── 02_Sentinel2_Rectangle_LULC_Classification.ipynb
├── 03_Sentinel1_SAR_Fundamentals.ipynb
├── 04_Sentinel1_Multitemporal_LULC_Classification.ipynb
├── 05_Sentinel1_Sentinel2_Data_Fusion.ipynb
│
└── data/
    └── phitsanulok_lulc_points.csv
```

---

# Troubleshooting

## Earth Engine project initialization

กำหนด Google Cloud Project ที่เปิดใช้ Earth Engine แล้ว

```python
PROJECT = "YOUR_GOOGLE_CLOUD_PROJECT_ID"
```

## Reference CSV not found

ตรวจว่า repository มี

```text
data/phitsanulok_lulc_points.csv
```

## Validation samples disappear after clipping

อย่า clip predictor image ด้วย final mapping boundary ก่อน sample reference points

```text
prepare predictors over reference domain
        ↓
sample training / validation
        ↓
classify
        ↓
clip final map
```

## `relativeOrbitNumber_start` conversion error

Earth Engine histogram keys อาจถูกส่งกลับเป็น string เช่น `"62.0"`

```python
RELATIVE_ORBIT = int(float(relative_orbit_key))
```

## `Geometry.contains()` returns Boolean

```python
inside_flag = ee.Number(
    ee.Algorithms.If(
        inside,
        1,
        0,
    )
).int()
```

---

# Recommended learning approach

```text
Read the concept
      ↓
Run one cell
      ↓
Inspect the map / table / graph
      ↓
Explain what changed
      ↓
Continue to the next cell
```

ไม่แนะนำให้ `Run all` ตั้งแต่ครั้งแรกโดยยังไม่อ่านผลของแต่ละขั้นตอน

---

# Further learning

▶️ **Google Earth Engine / Remote Sensing Teaching Playlist**  
https://www.youtube.com/playlist?list=PL2e-NEAjUyLEThjWtOqUyVtzBZcIm_Ha4

### Documentation

- [Google Earth Engine Python API](https://developers.google.com/earth-engine/guides/python_install)
- [Sentinel-2 SR Harmonized](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)
- [Sentinel-1 GRD](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S1_GRD)
- [Sentinel-1 Algorithms](https://developers.google.com/earth-engine/guides/sentinel1)
- [Random Forest in Earth Engine](https://developers.google.com/earth-engine/apidocs/ee-classifier-smilerandomforest)
- [Earth Engine `sampleRegions`](https://developers.google.com/earth-engine/apidocs/ee-image-sampleregions)
- [Earth Engine Error Matrix](https://developers.google.com/earth-engine/apidocs/ee-featurecollection-errormatrix)
- [Folium](https://python-visualization.github.io/folium/)
- [Pandas](https://pandas.pydata.org/)
- [NumPy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)

---

# Instructor and developer

**Assoc. Prof. Dr. Nattapon Mahavik**  
Environmental Science  
Faculty of Agriculture, Natural Resources and Environment  
Naresuan University, Thailand

**รศ.ดร.นัฐพล มหาวิค**  
สาขาวิทยาศาสตร์สิ่งแวดล้อม  
คณะเกษตรศาสตร์ ทรัพยากรธรรมชาติและสิ่งแวดล้อม  
มหาวิทยาลัยนเรศวร

▶️ [YouTube Teaching Playlist](https://www.youtube.com/playlist?list=PL2e-NEAjUyLEThjWtOqUyVtzBZcIm_Ha4)

---

# Suggested citation

If you use or adapt these teaching materials, please acknowledge the repository and the original teaching materials:

> Mahavik, N. *Teach-GEE-LULC: Teaching Land Use / Land Cover Classification with Google Earth Engine Python API, Sentinel-1 and Sentinel-2*. GitHub repository, Naresuan University.

Repository:  
https://github.com/nattaponm/Teach-GEE-LULC

---

# Educational use

This repository is intended primarily for **teaching, learning, demonstration, and methodological experimentation**.

Users who adapt the materials for other courses, research, publications, or derivative repositories should appropriately acknowledge the original teaching materials and relevant external data/software sources.

---

**Observe → Interpret → Sample → Classify → Validate → Compare → Explain**
