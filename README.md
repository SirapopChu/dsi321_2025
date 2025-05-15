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

ระบบนี้ถูกพัฒนาขึ้นเพื่อ **ติดตามและวิเคราะห์ข้อมูลสาธารณะ** ที่เกี่ยวข้องกับมหาวิทยาลัยธรรมศาสตร์ในเชิง **วิชาการ** โดยใช้เทคนิคการดึงข้อมูลแบบเรียลไทม์และการประมวลผลภาษาธรรมชาติ (NLP) เพื่อ:

- ตรวจสอบความคิดเห็นและบทความที่กล่าวถึง TU
- วิเคราะห์อารมณ์และหัวข้อของเนื้อหา
- แจ้งเตือนฝ่ายประชาสัมพันธ์เมื่อพบข้อมูลสำคัญ
- ปรับกลยุทธ์การสื่อสารให้เหมาะสมกับสถานการณ์
- วิเคราะห์สภาวะความเห็นสาธารณะต่อมหาวิทยาลัย

---

## ✨ Project Features

- ✅ Real-time Scraping จาก Twitter (X) ทุก 15 นาที 
- ✅ แปลงข้อมูลเป็น Parquet และจัดเก็บใน lakeFS
- ✅ ตรวจจับข้อมูลใหม่ผ่านการ hash และเปรียบเทียบ
- ✅ วิเคราะห์ด้วย NLP (Sentiment, Topic Modeling)
- ✅ Streamlit Dashboard แสดงผลในรูปแบบที่เข้าใจง่าย
- ✅ Orchestrated ด้วย Prefect และ Deploy ได้หลายแบบ

---

## 🏗️ System Architecture

![System Architecture](./path-to-your-image.png)

**Flow Summary:**

1. ผู้ใช้โพสต์ข้อความบน X → ระบบเริ่ม scraping
2. ตรวจสอบ hash กับข้อมูลเดิมจาก `lakeFS`
3. หากพบข้อมูลใหม่ → บันทึกข้อมูล + อัปเดต repository
4. โหลดข้อมูลไปยัง lakefs และ แสดงผลด้วย Dashboard ผ่าน Streamlit
5. orchestrate pipeline ทั้งหมด ด้วย Prefect

---

## 🧪 Technologies

| Component           | Technology             |
|---------------------|------------------------|
| Backend             | Python, FastAPI        |
| Scraping            | Playwright             |
| Storage             | lakeFS, Parquet        |
| Data Validation     | Pydantic               |
| NLP(word cloud)     | Gemini 2 Flash         |
| Dashboard           | Streamlit              |
| Orchestration       | Prefect                |
| Deployment          | Docker, GitHub Actions |

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
