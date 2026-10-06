# Teach-GEE-LULC

## Teaching Land Use / Land Cover Classification with Google Earth Engine Python API

**Sentinel-2 Optical Remote Sensing · Sentinel-1 SAR · Random Forest · Accuracy Assessment · Multitemporal Analysis · Data Fusion**

[![GitHub](https://img.shields.io/badge/GitHub-Teach--GEE--LULC-181717?logo=github)](https://github.com/nattaponm/Teach-GEE-LULC)
[![Google Colab](https://img.shields.io/badge/Google-Colab-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/01_Sentinel2_Point_LULC_Classification.ipynb)
[![YouTube](https://img.shields.io/badge/YouTube-Teaching%20Playlist-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/playlist?list=PL2e-NEAjUyLEThjWtOqUyVtzBZcIm_Ha4)
[![Earth Engine](https://img.shields.io/badge/Google-Earth%20Engine-4285F4?logo=googleearthengine&logoColor=white)](https://developers.google.com/earth-engine)
[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Sentinel-2](https://img.shields.io/badge/Data-Sentinel--2-2E8B57)](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)
[![Sentinel-1](https://img.shields.io/badge/Data-Sentinel--1-4169E1)](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S1_GRD)

---

## About this teaching repository

Repository นี้จัดทำขึ้นเพื่อใช้เป็นสื่อการเรียนการสอนด้าน **Remote Sensing, Geoinformatics, Environmental Science และ Land Use / Land Cover (LULC) Classification** โดยใช้ **Google Earth Engine (GEE) Python API** บน **Google Colab** เป็นแพลตฟอร์มหลัก

พื้นที่ตัวอย่างคือ **จังหวัดพิษณุโลก ประเทศไทย** โดยใช้ข้อมูล Sentinel-2 และ Sentinel-1 เพื่อให้ผู้เรียนค่อย ๆ พัฒนาความเข้าใจจากการอ่านภาพดาวเทียม การออกแบบ training samples การจำแนกด้วย Random Forest การประเมินความถูกต้อง การวิเคราะห์ SAR หลายช่วงเวลา และการรวมข้อมูล Optical + SAR

หลักการสำคัญของชุดการสอนนี้คือ

> **Readable code > compact code**  
> **One code cell = one concept**  
> **Scientific interpretation > running code without understanding**

จุดประสงค์จึงไม่ใช่เพียง “รันโค้ดให้ได้ผลลัพธ์” แต่ต้องเข้าใจว่า **sensor วัดอะไร, ตัวแปรมีความหมายอย่างไร, reference samples ถูกสร้างอย่างไร, model เรียนรู้อะไร และผลลัพธ์มีข้อจำกัดอะไร**

---

## Teaching origin and code development

แนวคิดการเรียนการสอนและตัวอย่างโค้ดใน repository นี้ **พัฒนาและดัดแปลงต่อยอดจากชุดวิดีโอการสอนด้าน Google Earth Engine, Remote Sensing และ Geospatial Analysis ของ รศ.ดร.นัฐพล มหาวิค**  
สาขาวิทยาศาสตร์สิ่งแวดล้อม คณะเกษตรศาสตร์ ทรัพยากรธรรมชาติและสิ่งแวดล้อม มหาวิทยาลัยนเรศวร

ชุด Notebook ใน repository นี้ได้นำแนวคิดจากสื่อการสอนเดิมมาปรับโครงสร้างใหม่ให้อยู่ในรูปแบบ

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
GeoTIFF / CSV outputs for further GIS analysis
```

▶️ **YouTube Teaching Playlist**  
https://www.youtube.com/playlist?list=PL2e-NEAjUyLEThjWtOqUyVtzBZcIm_Ha4

> **YouTube explains the concepts; GitHub organizes the workflow; Colab lets students reproduce the analysis.**  
> **YouTube ใช้อธิบายแนวคิด GitHub ใช้จัดระบบบทเรียน และ Google Colab ใช้ทดลองและทำซ้ำการวิเคราะห์ด้วยตนเอง**

---

# Course philosophy

แนวทางการเรียนรู้ของ repository นี้คือ

$$
\boxed{
\text{Observe}
\rightarrow
\text{Interpret}
\rightarrow
\text{Sample}
\rightarrow
\text{Classify}
\rightarrow
\text{Validate}
\rightarrow
\text{Compare}
\rightarrow
\text{Explain}
}
$$

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

แต่ละ Notebook ถูกออกแบบให้ **รันได้แบบ standalone** ขณะที่แนวคิดการเรียนจะต่อเนื่องจากบทก่อนหน้า

---

# Notebooks

| No. | Notebook | Main question | Main concepts | GitHub | Colab |
|---|---|---|---|---|---|
| 01 | Sentinel-2 Point LULC Classification | จุดตัวอย่างสามารถใช้จำแนก LULC ได้อย่างไร? | Sentinel-2, spectral indices, Random Forest, confusion matrix | [View](01_Sentinel2_Point_LULC_Classification.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/01_Sentinel2_Point_LULC_Classification.ipynb) |
| 02 | Sentinel-2 Rectangle LULC Classification | Spatial support ของ training sample มีผลอย่างไร? | Point vs rectangle, mixed pixels, edge effects, training pixels | [View](02_Sentinel2_Rectangle_LULC_Classification.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/02_Sentinel2_Rectangle_LULC_Classification.ipynb) |
| 03 | Sentinel-1 SAR Fundamentals | SAR วัดอะไร และอ่าน VV/VH อย่างไร? | Active sensing, backscatter, dB, VV/VH, scattering, speckle, temporal profiles | [View](03_Sentinel1_SAR_Fundamentals.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/03_Sentinel1_SAR_Fundamentals.ipynb) |
| 04 | Sentinel-1 Multitemporal LULC Classification | Temporal SAR ช่วยการจำแนกหรือไม่? | Same-date mosaic, monthly VV/VH, January vs annual model, variable importance | [View](04_Sentinel1_Multitemporal_LULC_Classification.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/04_Sentinel1_Multitemporal_LULC_Classification.ipynb) |
| 05 | Sentinel-1 + Sentinel-2 Data Fusion | Optical และ SAR ให้ข้อมูลเสริมกันหรือไม่? | Feature-level fusion, common validation support, sensor importance, disagreement | [View](05_Sentinel1_Sentinel2_Data_Fusion.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teach-GEE-LULC/blob/main/05_Sentinel1_Sentinel2_Data_Fusion.ipynb) |

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

> **หมายเหตุ:** Public notebooks ไม่ควรใช้ Google Cloud Project ID ส่วนบุคคลของผู้สอน

---

# Core tools and libraries

[![Earth Engine](https://img.shields.io/badge/Google-Earth%20Engine-Python%20API-4285F4?logo=googleearthengine&logoColor=white)](https://developers.google.com/earth-engine/guides/python_install)
[![Google Colab](https://img.shields.io/badge/Google-Colab-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/)
[![Folium](https://img.shields.io/badge/Library-Folium-77B829)](https://python-visualization.github.io/folium/)
[![Pandas](https://img.shields.io/badge/Library-pandas-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/Library-NumPy-013243?logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-11557C)](https://matplotlib.org/)

### Main libraries

```python
import ee
import folium
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

`ee.Classifier.smileRandomForest()` ของ Google Earth Engine เป็น classifier หลักของชุดการสอนนี้ จึงไม่จำเป็นต้องใช้ scikit-learn ใน workflow หลัก

---

# Earth Engine datasets

### Sentinel-2 Surface Reflectance Harmonized

[`COPERNICUS/S2_SR_HARMONIZED`](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)

ใช้สำหรับ

- visible reflectance
- NIR
- SWIR
- NDVI
- NDWI
- NDBI
- optical LULC classification

### Sentinel-1 GRD

[`COPERNICUS/S1_GRD`](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S1_GRD)

ใช้สำหรับ

- VV backscatter
- VH backscatter
- SAR interpretation
- multitemporal analysis
- optical–SAR data fusion

### Administrative boundary

[`FAO/GAUL/2025/level2`](https://developers.google.com/earth-engine/datasets/catalog/FAO_GAUL_2025_level2)

ใช้กำหนดพื้นที่แสดงผลระดับอำเภอ

---

# Reference data

ไฟล์ reference samples อยู่ใน

```text
data/phitsanulok_lulc_points.csv
```

ใช้ 5 classes

| Class ID | Class |
|---:|---|
| 0 | Urban / Built-up |
| 1 | Water |
| 2 | Forest / Tree cover |
| 3 | Agriculture |
| 4 | Bare soil / Open land |

ชุดข้อมูลนี้ใช้สำหรับ **teaching and methodological demonstration** ไม่ใช่ probability-based regional accuracy assessment dataset

---

# Core concepts and equations

GitHub รองรับ mathematical expressions ใน Markdown ดังนั้นสมการด้านล่างสามารถ render ได้โดยตรงด้วย `$$ ... $$`

<details>
<summary><b>Notebook 01 — Sentinel-2 Point Classification</b></summary>

## Surface reflectance scaling

Sentinel-2 Surface Reflectance digital numbers ถูก scale เป็น reflectance:

$$
\rho = DN \times 10^{-4}
$$

## NDVI

$$
NDVI =
\frac{B8-B4}{B8+B4}
$$

NDVI ใช้วัด relative vegetation greenness แต่

$$
NDVI \neq \text{Forest class}
$$

## NDWI

$$
NDWI =
\frac{B3-B8}{B3+B8}
$$

และ

$$
NDWI \neq \text{Water class}
$$

## NDBI

$$
NDBI =
\frac{B11-B8}{B11+B8}
$$

และ

$$
NDBI \neq \text{Urban class}
$$

indices เหล่านี้เป็น **predictor variables** ไม่ใช่ class labels

## Sentinel-2 feature vector

$$
\mathbf{x}_{S2}
=
[
B2,B3,B4,B8,B11,B12,
NDVI,NDWI,NDBI
]
$$

## Random Forest classification

ถ้ามี decision trees จำนวน $B$ ต้น

$$
\hat y
=
\operatorname{mode}
[
h_1(\mathbf{x}),
h_2(\mathbf{x}),
\dots,
h_B(\mathbf{x})
]
$$

## Confusion matrix

ให้ $n_{ij}$ เป็นจำนวน reference samples ของ class $i$ ที่ถูกจำแนกเป็น class $j$

### Overall Accuracy

$$
OA=
\frac{\sum_i n_{ii}}{N}
$$

### Producer's Accuracy

$$
PA_i=
\frac{n_{ii}}
{\sum_j n_{ij}}
$$

### User's Accuracy

$$
UA_i=
\frac{n_{ii}}
{\sum_j n_{ji}}
$$

### F1 score

$$
F1_i=
2
\frac{PA_iUA_i}
{PA_i+UA_i}
$$

</details>

---

<details>
<summary><b>Notebook 02 — Training Geometry and Spatial Support</b></summary>

## Training-window area

สำหรับ rectangle กว้าง $w$ และสูง $h$

$$
A_{window}=w\times h
$$

สำหรับ 20 × 20 m:

$$
A_{window}=400~m^2
$$

สำหรับ Sentinel-2 10-m pixel:

$$
A_{pixel}\approx10\times10=100~m^2
$$

จำนวน output-grid pixels โดยประมาณ:

$$
n
\approx
\frac{A_{window}}
{A_{pixel}}
$$

ดังนั้น 20 × 20 m window ให้ประมาณ 4 output-grid samples แต่จำนวนจริงขึ้นกับ pixel-grid alignment, projection และ masking

## Mixed pixel

ค่าที่ sensor วัดสามารถเขียนแนวคิดอย่างง่ายได้ว่า

$$
R_{pixel}
\approx
\sum_{k=1}^{K}f_kR_k
$$

โดย

$$
\sum_{k=1}^{K}f_k=1
$$

## Important sampling concept

$$
n_{pixels}
\neq
n_{independent\ locations}
$$

และ

> **Training quantity ≠ Training quality**

</details>

---

<details>
<summary><b>Notebook 03 — Sentinel-1 SAR Fundamentals</b></summary>

## Radar backscatter in decibels

$$
\sigma^0_{dB}
=
10\log_{10}
\left(
\sigma^0_{linear}
\right)
$$

ย้อนกลับ:

$$
\sigma^0_{linear}
=
10^{\sigma^0_{dB}/10}
$$

ดังนั้น -10 dB มี backscatter สูงกว่า -20 dB

## VV and VH

```text
VV = Vertical transmit / Vertical receive
VH = Vertical transmit / Horizontal receive
```

## Polarization contrast

$$
D_{VV-VH}
=
VV_{dB}-VH_{dB}
$$

และ

$$
VV_{dB}-VH_{dB}
=
10\log_{10}
\left(
\frac{VV_{linear}}
{VH_{linear}}
\right)
$$

## Radar response

Backscatter ไม่ได้ขึ้นกับ land cover เพียงอย่างเดียว

$$
\sigma^0
=
f(
\text{roughness},
\text{moisture},
\text{structure},
\theta_i,
\text{geometry},
\dots
)
$$

## Temporal backscatter profile

สำหรับ class $c$ และเดือน $m$

$$
\tilde{\sigma}^{0}_{c,m}
=
\operatorname{median}
\left(
\sigma^{0}_{i,m}
\right)
$$

## Annual SAR feature vector

$$
\mathbf{x}_{S1}
=
[
VV_{Jan},VH_{Jan},
\dots,
VV_{Dec},VH_{Dec}
]
$$

ดังนั้น

$$
p=24
$$

</details>

---

<details>
<summary><b>Notebook 04 — Sentinel-1 Multitemporal Classification</b></summary>

## January baseline

$$
\mathbf{x}^{Jan}
=
[
VV_{Jan},VH_{Jan}
]
$$

ดังนั้น

$$
p=2
$$

## Annual multitemporal SAR

$$
\mathbf{x}^{Annual}
=
[
VV_{Jan},VH_{Jan},
\dots,
VV_{Dec},VH_{Dec}
]
$$

ดังนั้น

$$
p=24
$$

## Model improvement

$$
\Delta OA
=
OA_{Annual}
-
OA_{Jan}
$$

สำหรับ class $i$

$$
\Delta F1_i
=
F1_{Annual,i}
-
F1_{Jan,i}
$$

## Normalized variable importance

$$
I_j^*
=
\frac{I_j}
{\sum_{k=1}^{p}I_k}
$$

โดย

$$
\sum_j I_j^*=1
$$

## Importance aggregated by month

$$
I_m
=
I_{VV_m}
+
I_{VH_m}
$$

### Important interpretation rule

$$
\text{Variable importance}
\neq
\text{Causation}
$$

</details>

---

<details>
<summary><b>Notebook 05 — Sentinel-1 + Sentinel-2 Data Fusion</b></summary>

## Sentinel-2 feature space

$$
\mathbf{x}_{S2}\in\mathbb{R}^{9}
$$

## January Sentinel-1

$$
\mathbf{x}_{S1,Jan}\in\mathbb{R}^{2}
$$

## Same-period fusion

$$
\mathbf{x}_{Fusion,Jan}
=
[
\mathbf{x}_{S2},
\mathbf{x}_{S1,Jan}
]
$$

ดังนั้น

$$
p=11
$$

## Optical + annual SAR fusion

$$
\mathbf{x}_{Fusion,Annual}
=
[
\mathbf{x}_{S2},
\mathbf{x}_{S1,Annual}
]
$$

ดังนั้น

$$
p=33
$$

## Common valid-data support

เพื่อให้ models ถูกเปรียบเทียบบน spatial support เดียวกัน

$$
M_{common}
=
M_{S2}
\cap
M_{S1}
$$

## Sensor-level importance

$$
I_{S2}
=
\sum_{j\in S2}
I_j^*
$$

$$
I_{S1}
=
\sum_{j\in S1}
I_j^*
$$

## Spatial disagreement

สำหรับ maps สองชุด $C_A(x)$ และ $C_B(x)$

$$
D(x)=
\begin{cases}
0,& C_A(x)=C_B(x)\\
1,& C_A(x)\neq C_B(x)
\end{cases}
$$

### Important interpretation rule

$$
\text{Disagreement}
\neq
\text{Error}
$$

และ

$$
\boxed{
\text{More predictors}
\neq
\text{better model}
}
$$

</details>

---

# Example teaching results

ผลต่อไปนี้เป็น **ตัวอย่างจาก reference dataset และ hold-out samples ที่ใช้ในชุดการสอนนี้เท่านั้น** ไม่ควรตีความเป็น publication-grade regional accuracy assessment

| Model | Predictors | Overall Accuracy | Mean F1 |
|---|---:|---:|---:|
| Sentinel-2 January | 9 | 93.3% | 0.933 |
| Sentinel-1 January | 2 | 70.0% | 0.686 |
| Sentinel-2 + Sentinel-1 January | 11 | **96.7%** | **0.966** |
| Sentinel-2 + Annual Sentinel-1 | 33 | 93.3% | 0.931 |

ตัวอย่างนี้แสดงว่า same-period optical–SAR fusion ให้ผลดีที่สุดใน hold-out sample ชุดนี้ ขณะที่การเพิ่ม temporal predictors จำนวนมากไม่ได้ทำให้ accuracy สูงขึ้นเสมอ

$$
\boxed{
\text{More data}
\neq
\text{more useful information}
}
$$

> Validation set มีจำนวนจำกัด ดังนั้นผลต่างเพียงหนึ่ง validation point สามารถเปลี่ยน Overall Accuracy ได้หลาย percentage points ผลลัพธ์จึงควรใช้เพื่อการเรียนรู้และเปรียบเทียบ methodology มากกว่าการอ้างความแม่นยำระดับภูมิภาค

---

# Scientific interpretation rules

1. **Do not interpret an index as a class.**  
   NDVI ไม่ใช่ Forest, NDWI ไม่ใช่ Water และ NDBI ไม่ใช่ Urban โดยอัตโนมัติ

2. **Do not interpret training accuracy as map accuracy.**

3. **More sampled pixels do not mean more independent reference locations.**

4. **Variable importance is not causation.**

5. **Disagreement between maps is not automatically error.**

6. **More predictors do not guarantee a better model.**

7. **Always inspect imagery before interpreting numerical results.**

8. **Always report validation sample size.**

9. **Training extent and final mapping extent may be different.**

10. **Class definitions must remain scientifically meaningful through time.**

---

# Outputs

Notebooks สามารถ export ผลลัพธ์ไปยัง Google Drive เพื่อใช้ต่อใน QGIS หรือ GIS software อื่น

ตัวอย่าง:

```text
PHS_S2_Point_RF_LULC_2021.tif
PHS_S2_Rectangle_RF_LULC_2021.tif
PHS_S1_January_RF_LULC_2021.tif
PHS_S1_Annual_RF_LULC_2021.tif
PHS_S2_S1_Annual_Fusion_RF_LULC_2021.tif
```

โดยทั่วไปใช้

```text
CRS   = EPSG:32647
Scale = 10 m
NoData = 255
```

และสามารถ export ตาราง เช่น

```text
Random Forest variable importance
Model comparison
Reference sample tables
```

เป็น CSV ได้

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

> หากเปลี่ยนชื่อไฟล์ Notebook ใน GitHub ต้องแก้ทั้ง **GitHub link และ Colab link ใน README ให้ตรงกันทุกตัวอักษร**

---

# Troubleshooting

## 1. Earth Engine project initialization

แก้

```python
PROJECT = "YOUR_GOOGLE_CLOUD_PROJECT_ID"
```

เป็น Google Cloud Project ที่เปิดใช้งาน Earth Engine แล้ว

---

## 2. Reference CSV not found

ตรวจว่า repository มี

```text
data/phitsanulok_lulc_points.csv
```

Notebook จะพยายามโหลดจาก GitHub และสามารถ upload จากเครื่องได้หากจำเป็น

---

## 3. Validation samples disappear after clipping

อย่า clip predictor image ด้วย final map boundary ก่อน sample reference points

ใช้หลัก

```text
prepare predictors over reference domain
        ↓
sample training / validation
        ↓
classify
        ↓
clip final map
```

---

## 4. `relativeOrbitNumber_start` conversion error

Earth Engine histogram keys อาจถูกส่งกลับเป็น string เช่น

```text
"62.0"
```

จึงควรใช้

```python
RELATIVE_ORBIT = int(float(relative_orbit_key))
```

---

## 5. `Geometry.contains()` returns Boolean

`contains()` คืนค่า server-side Boolean จึงไม่ควรใช้ `ee.Number(boolean)` โดยตรง

ตัวอย่าง:

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

สำหรับนิสิต แนะนำให้ทำทุก Notebook ด้วยลำดับ

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

ไม่ควรรัน `Run all` ตั้งแต่ครั้งแรกโดยยังไม่อ่านผลของแต่ละขั้นตอน

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

## Suggested citation

If you use or adapt these teaching materials, please acknowledge the repository and the original teaching materials:

> Mahavik, N. *Teach-GEE-LULC: Teaching Land Use / Land Cover Classification with Google Earth Engine Python API, Sentinel-1 and Sentinel-2*. GitHub repository, Naresuan University.

Repository:  
https://github.com/nattaponm/Teach-GEE-LULC

---

## License and educational use

This repository is intended primarily for **teaching, learning, demonstration, and methodological experimentation**.

Users who adapt the materials for other courses, research, publications, or derivative repositories should appropriately acknowledge the original teaching materials and relevant external data/software sources.

---

**Observe → Interpret → Sample → Classify → Validate → Compare → Explain**
