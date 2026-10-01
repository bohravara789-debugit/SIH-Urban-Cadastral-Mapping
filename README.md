# SIH-Urban-Cadastral-Mapping
# 🛰️ AI-Based Automated Urban Parcel Mapping & Cadastral Feature Extraction

### Smart India Hackathon 2026 · SIH26012 · Smart Automation

> **An AI-powered approach to extracting urban cadastral features from drone and aerial imagery, reducing manual interpretation and accelerating GIS-based mapping workflows.**

---

## 🌆 Overview

Urban planning, land management, taxation, infrastructure development, and public services rely heavily on accurate cadastral information.

However, extracting and updating cadastral features from aerial or drone imagery often involves **manual image interpretation and field-based Ground Truthing (GT)**. This makes the process time-consuming, resource-intensive, and dependent on human intervention.

Our project proposes an **AI + Computer Vision + GIS pipeline** that can automatically identify urban features from aerial imagery, extract their boundaries, and convert them into structured geospatial data.

### 🎯 Our Vision

**Drone Image → AI Detection → Feature Boundaries → GIS Data → Interactive Map**

---

## ✨ Key Features

| Feature                              | Description                                            |
| ------------------------------------ | ------------------------------------------------------ |
| 🛰️ **Aerial Image Processing**      | Accept drone and aerial imagery as input               |
| 🤖 **AI-Based Segmentation**         | Identify relevant urban features using computer vision |
| 🏢 **Building Footprint Extraction** | Detect and extract building boundaries                 |
| 📐 **Boundary Extraction**           | Convert segmentation masks into usable geometries      |
| 🗺️ **GIS Integration**              | Generate GIS-compatible spatial data                   |
| 📄 **GeoJSON Output**                | Store extracted features in a structured format        |
| 📊 **Confidence Information**        | Provide prediction confidence for detected features    |
| 🌐 **Interactive Visualization**     | Display results through a web-based interface          |
| 🔄 **Scalable Architecture**         | Designed for future multi-feature cadastral mapping    |

---

# 🧠 Proposed Solution

The system combines **Artificial Intelligence, Computer Vision, and Geographic Information Systems (GIS)** into a single workflow.

```text
                  ┌─────────────────────┐
                  │  🛰️ Drone / Aerial  │
                  │       Imagery       │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │  Image Preprocessing│
                  │       OpenCV        │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │   🤖 AI Segmentation │
                  │   YOLO-based Model  │
                  └──────────┬──────────┘
                             │
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
         🏢 Buildings     🗺️ Parcels      🛣️ Roads
              │              │              │
              └──────────────┼──────────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │ Boundary Extraction │
                  │   OpenCV / Shapely  │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │  GIS Data Generation│
                  │   GeoPandas/GeoJSON │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │ 🗺️ Visualization     │
                  │ Streamlit + Folium  │
                  └─────────────────────┘
```

---

# 🎯 Objectives

* Automate the extraction of urban features from aerial imagery.
* Reduce manual effort in cadastral feature identification.
* Extract building footprints and other relevant urban features.
* Convert detected boundaries into structured geospatial data.
* Generate GIS-compatible outputs such as GeoJSON.
* Provide confidence information for AI predictions.
* Visualize extracted features through an interactive interface.
* Establish a scalable foundation for automated cadastral mapping.

---

# 🛠️ Technology Stack

### 💻 Core

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge\&logo=python\&logoColor=white)

### 🤖 AI & Computer Vision

![YOLO](https://img.shields.io/badge/YOLO-Segmentation-111111?style=for-the-badge)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?style=for-the-badge\&logo=opencv\&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?style=for-the-badge\&logo=numpy\&logoColor=white)

### 🗺️ GIS & Geospatial Processing

![GeoPandas](https://img.shields.io/badge/GeoPandas-GIS-139C5A?style=for-the-badge)
![Shapely](https://img.shields.io/badge/Shapely-Geometries-4B8BBE?style=for-the-badge)

### 🌐 Application & Visualization

![Streamlit](https://img.shields.io/badge/Streamlit-App-FF4B4B?style=for-the-badge\&logo=streamlit\&logoColor=white)
![Folium](https://img.shields.io/badge/Folium-Interactive%20Maps-77B829?style=for-the-badge)

### 🔧 Development

![Git](https://img.shields.io/badge/Git-Version%20Control-F05032?style=for-the-badge\&logo=git\&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge\&logo=github\&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge\&logo=jupyter\&logoColor=white)

---

# 📂 Project Structure

```text
SIH-Urban-Cadastral-Mapping/
│
├── 📁 app/
│   ├── main.py
│   ├── preprocessing.py
│   ├── detection.py
│   ├── segmentation.py
│   ├── confidence.py
│   └── visualization.py
│
├── 📁 models/
│   └── README.md
│
├── 📁 data/
│   ├── sample_input/
│   └── sample_output/
│
├── 📁 gis/
│   └── geojson_generator.py
│
├── 📁 notebooks/
│   └── model_testing.ipynb
│
├── 📁 tests/
│
├── 📄 requirements.txt
├── 📄 .gitignore
└── 📄 README.md
```

---

# ⚙️ How It Works

### 01 · 📥 Input

Upload a drone or aerial image of an urban area.

### 02 · 🧹 Preprocessing

The image is resized and processed using computer-vision techniques to prepare it for model inference.

### 03 · 🤖 AI Segmentation

The AI model analyses the image and identifies relevant urban features.

### 04 · 📐 Boundary Extraction

Predicted segmentation masks are processed to obtain feature boundaries and polygon geometries.

### 05 · 🗺️ Geospatial Conversion

The extracted geometries are converted into GIS-compatible structures such as **GeoJSON**.

### 06 · 📊 Visualization

The detected features, boundaries, confidence information, and map output are presented through the application interface.

---

# 📊 Expected Output

The prototype aims to generate:

```text
🛰️ Input Aerial Image
        ↓
🤖 AI Predictions
        ↓
🏢 Building / Urban Feature Masks
        ↓
📐 Extracted Boundaries
        ↓
📄 GeoJSON Features
        ↓
🗺️ Interactive GIS Visualization
```

### Example Output Components

* Original aerial image
* AI-generated segmentation mask
* Extracted feature boundaries
* Confidence values
* GeoJSON file
* Interactive map visualization

> **Note:** Geospatial accuracy depends on the availability and quality of georeferenced imagery and the associated spatial information.

---

# 🚧 Current Scope

The **initial prototype focuses on building footprint extraction from aerial imagery**.

The modular architecture allows future expansion toward:

* 🗺️ Parcel boundary extraction
* 🛣️ Road extraction
* 🏗️ Infrastructure mapping
* 🌳 Additional urban feature classes
* 📍 Georeferenced cadastral mapping
* 👤 Human-in-the-loop Ground Truthing
* 🏙️ Large-scale urban processing

---

# 🔮 Future Scope

### AI Improvements

* Fine-tuning on high-resolution drone imagery
* Multi-class urban feature segmentation
* Improved boundary refinement
* Continuous model improvement using verified data

### GIS Improvements

* Advanced coordinate transformation
* Integration with existing GIS platforms
* Automated spatial validation
* Large-scale geospatial processing

### Operational Improvements

* Human verification and correction workflow
* Batch processing of multiple drone images
* Integration with municipal/land-record systems
* Scalable cloud deployment

---

# 📈 Development Roadmap

```text
[✓] Project Architecture
       ↓
[✓] GitHub Repository
       ↓
[ ] Dataset Selection
       ↓
[ ] AI Model Testing
       ↓
[ ] Building Segmentation
       ↓
[ ] Boundary Extraction
       ↓
[ ] GeoJSON Generation
       ↓
[ ] Streamlit Interface
       ↓
[ ] GIS Visualization
       ↓
[ ] Testing & Evaluation
       ↓
[ ] Final SIH Prototype 🚀
```

---

# 👥 Team

### Smart India Hackathon 2026

**Problem Statement:** `SIH26012`

**Domain:** Smart Automation

**Project:** AI-Based Automated Urban Parcel Mapping and Cadastral Feature Extraction System using Drone Imagery

---

# 📌 Project Status

> 🚧 **Prototype Under Development**

The project architecture and GitHub repository have been established. AI model integration, feature segmentation, boundary extraction, GIS conversion, visualization, and evaluation are being developed incrementally.

---

# ⚠️ Important Note

This project is developed as a **prototype for Smart India Hackathon 2026**.

AI-generated feature boundaries are intended to assist cadastral mapping workflows and should **not be considered legally authoritative land boundaries** without appropriate surveying, ground verification, and official validation.

---

# 📜 License

This project is developed for educational, research, and hackathon purposes.

---

<div align="center">

### 🛰️ From Aerial Imagery to Intelligent Cadastral Mapping

**SIH 2026 · SIH26012 · Smart Automation**

</div>
