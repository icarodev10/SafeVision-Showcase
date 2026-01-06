# 👁️ SafeVision – Intelligent PPE Monitoring System

> A real-time computer vision system designed to automate safety compliance in industrial environments using Deep Learning.

![Status](https://img.shields.io/badge/Status-Portfolio%20Demo-blue?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)
![YOLOv8](https://img.shields.io/badge/AI-YOLOv8-purple?style=for-the-badge)
![FastAPI](https://img.shields.io/badge/Backend-FastAPI-green?style=for-the-badge)

## 🎥 Project Demo

https://github.com/user-attachments/assets/7c2a13ed-d7ac-47b6-8909-87992b785fb5

---

## 💡 About The Project

**SafeVision** was developed to solve a crucial problem in Industry 4.0: manual monitoring of Personal Protective Equipment (PPE) is inefficient and prone to error.

This system uses advanced Computer Vision to monitor live camera feeds, detecting whether workers are wearing required safety gear (Helmets, Goggles, Gloves). Unlike simple object detectors, **SafeVision implements relational logic**: it validates if the PPE is actually *on* the person, reducing false positives.

### 🚀 Key Features

* **🧠 Context-Aware Detection:** Uses a custom-trained YOLOv8 model to detect *Persons* and *PPE* separately, validating compliance based on spatial proximity (IoU Logic).
* **⚡ Stabilized Real-Time Tracking:** Implements a temporal buffer ("Smoothing Algorithm") to prevent detection flickering and ensure robust tracking even when the camera shakes.
* **🚨 Automatic Incident Logging:** Upon detecting a violation (e.g., "No Helmet"), the system automatically captures a snapshot and logs the event to a MySQL database with a timestamp.
* **📊 Web Dashboard:** A FastAPI-integrated frontend for managers to view live streams, check safety statistics, and review incident history.

---

## 🛠️ Tech Stack & Architecture

Although the source code is restricted for portfolio purposes, the system is built on a modern, scalable stack:

* **AI Core:** Python, Ultralytics YOLOv8 (Custom Dataset), OpenCV.
* **Backend:** FastAPI (Async handling), WebSockets (Live streaming), Threading (Non-blocking alerts).
* **Database:** MySQL (Relational schema for multi-tenancy and logs).
* **Frontend:** HTML5, CSS3, JavaScript (Vanilla).

### 🧠 How the Logic Works (Simplified)
1.  **Detection:** The model identifies a `Person` and surrounding objects (`Helmet`, `Goggles`).
2.  **Geometry Check:** The algorithm calculates if the safety equipment is physically located *within* the bounding box of the person.
3.  **Stabilization:** If a violation is detected, it enters a "Buffer Memory". The alert persists for a few frames even if detection is momentarily lost, ensuring visual stability.
4.  **Action:** If the violation is confirmed, an alert is triggered visually and stored in the database.

---

## 🔒 Access & License

This project was developed as a **Project for Industrial Automation**.
The source code is currently **Closed Source** as it belongs to the development team and the institution.

This repository serves as a technical showcase of the engineering and logic applied.

---

## 👥 Development Team

This project was a collaborative effort developed at SENAI by:

* **Icaro de Souza de Lima** - [GitHub](https://github.com/icarodev10)
* **Luís Miguel da Costa** - [GitHub](https://github.com/LuisCosta321)
* **Marcos Vinícius Cavalaro** - [GitHub](https://github.com/MarcosCavalaro)
* **Kaique Borlenghi da Silva** - [GitHub](https://github.com/KaiqueBorlenghi)
* **Nicolas Eduardo de Godoy** - [GitHub](https://github.com/NicolasEGodoy)

---

### 📞 Contact
Interested in the technology or implementation details? Feel free to reach out via LinkedIn!

### 📞 Contact
Interested in the Computer Vision implementation or the backend architecture? Feel free to reach out via LinkedIn!
