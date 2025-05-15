# DSI321_2025
# 📡 Realtime x Scraping for Adjusting TU Academic Public Relations

## Table of Contents

- [Project Overview](#project-overview)
- [Group Information](#group-information)
- [Project Features](#project-features)
- [System Architecture](#system-architecture)
- [Technologies](#technologies)
- [Deployment Guide](#deployment-guide)

---

## 📘 Project Overview

This system was developed to **Track and analyze public data** related to Thammasat University in **academic** terms using real-time data extraction and natural language processing (NLP) techniques to:

- Check comments and articles mentioning TU
- Analyze the sentiment and topic of the content
- Alert the PR department when important information is found
- Adjust the communication strategy to suit the situation
- Analyze the public opinion situation on the university

---

## ✨ Project Features

- ✅ Real-time Scraping from Twitter (X) every 15 minutes
- ✅ Convert data to Parquet and store in lakeFS
- ✅ Detect new data through hashing and comparison
- ✅ Analyze with NLP (Sentiment, Topic Modeling)
- ✅ Streamlit Dashboard shows the results in an easy-to-understand format
- ✅ Orchestrated with Prefect and can be deployed in multiple ways

---

## 🏗️ System Architecture

![System Architecture](./path-to-your-image.png)

**Flow Summary:**

1. User posts a message on X → System starts scraping
2. Check hash against original data from `lakeFS`
3. If new data is found → Save data + Update repository
4. Load data to lakefs and display with Dashboard via Streamlit
5. Orchestrate entire pipeline with Prefect

---

## 🧪 Technologies

| Component | Technology |
|---------------------|------------------------|
| Backend | Python, FastAPI |
| Scraping | Playwright |
| Storage | lakeFS, Parquet |
| Data Validation | Pydantic |
| NLP(word cloud) | Gemini 2 Flash |
| Dashboard | Streamlit |
| Orchestration | Prefect |
| Deployment | Docker, GitHub Actions |

---

## 🚀 Deployment Guide

### 🧰 Prerequisites

- Python 3.9+
- Docker + Docker Compose
- Git
-requirements.txt
---

### 🛠️ Manual Deployment

1. **Clone Repository:** 

```bash 
git clone https://github.com/SirapopChu/dsi321_2025 
cd Siapopchu/dsi321_2025
