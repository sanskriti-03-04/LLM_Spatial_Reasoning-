# 🌍 LLM-Based Spatial Reasoning System

**Natural Language ➝ Geospatial Maps with AI**  
Chain-of-Thought Reasoning | OSM Data | Chandigarh, India

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/YOUR_NOTEBOOK_ID_HERE)

> 🔗 Click the badge above to run the full notebook with maps and LLM logic on Google Colab.

---

## 🚀 Overview

This project turns plain English queries like:

> "Show roads within 500m of PGIMER hospital"

...into **geospatial workflows and visualizations** using a Large Language Model (LLM) and tools like `GeoPandas`, `Folium`, and `OpenStreetMap`.

The system reasons through each query step-by-step — geocoding, filtering, buffering, masking — to generate accurate maps.

---

## 🧠 Key Features

- ✅ Uses **GPT-4 (via LangChain)** for spatial query reasoning  
- 🗺️ Loads and filters **OpenStreetMap road data** using OSMnx  
- 📐 Performs spatial operations like **buffering**, **intersection**, and **masking**  
- 🧪 Visualizes results using **Folium interactive maps**  
- 🧵 Includes **Chain-of-Thought (CoT)** explanation for every query  

---

## 📍 Sample Queries

| Prompt | Operation |
|--------|-----------|
| 🟢 Roads within 500m of city center | Buffer + Intersect |
| 🟣 Major roads only | Filter by OSM tags |
| 🟡 Roads near PGIMER | Geocode + Buffer |
| 🟠 Roads in north Chandigarh | Region clip |
| 🔴 Roads far from flood zones | Exclude masked area |

All results are interactive and rendered directly in the notebook.

---

## 📊 Evaluation Metrics

| Query        | Roads Returned | Reasoning | Time |
|--------------|----------------|-----------|------|
| City Center  | 183            | ✅ Yes    | 1.3s |
| Major Roads  | 42             | ✅ Yes    | 0.9s |
| PGIMER Area  | 96             | ✅ Yes    | 1.5s |
| North Zone   | 121            | ✅ Yes    | 1.1s |
| Flood Zone   | 205            | ✅ Yes    | 1.7s |

---

## 🧰 Tech Stack

| Tool         | Role                        |
|--------------|-----------------------------|
| GPT-4 + LangChain | Natural language parsing |
| OSMnx         | Downloading road networks   |
| GeoPandas     | Spatial analysis & geometry |
| Folium        | Interactive maps            |
| Shapely       | Buffering & filtering       |
| Google Colab  | Notebook execution platform |

---

## 🧪 Reasoning Approach

Each query is handled in steps:
1. Parse intent using LLM (e.g., "near", "within", "exclude")
2. Geocode key locations
3. Generate spatial buffers or masks
4. Filter roads or features based on logic
5. Render results with map overlays

---

## 📂 Repository Contents

