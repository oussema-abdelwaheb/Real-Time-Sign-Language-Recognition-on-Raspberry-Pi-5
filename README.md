import os

# Define the project name and directory structure
project_name = "sign-language-pi"
repo_dir = project_name
src_dir = os.path.join(repo_dir, 'src')
model_dir = os.path.join(repo_dir, 'model')

# Define the content for each file

# README.md
readme_content = """
# 🖐️ Real-Time Sign Language Recognition on Raspberry Pi 5

A lightweight, fully offline **sign language recognition system** built using a **Raspberry Pi 5**, **USB webcam**, and a **2x16 I2C LCD**. This project uses a classical machine learning model trained on over **87,000 images** to detect and display 28 static American Sign Language (ASL) signs in real time.

---

## 📸 Project Overview

This system captures live video feed from a USB webcam, detects a hand gesture, classifies it into one of 28 ASL signs (A–Z + Space), and displays the translated letter on an I2C LCD screen.

Unlike most gesture recognition systems that rely on GPU-intensive deep learning models and cloud APIs, this project runs **entirely offline** on a Raspberry Pi using **classical ML**, optimized for edge performance.

---

## ✨ Features

- 🧠 Recognizes **28 ASL signs** (A–Z + Space)
- 🎯 Trained on **87,000+ labeled images** from a Kaggle dataset
- 🖥️ Real-time gesture capture and classification via webcam
- 📟 Output displayed on **2x16 I2C LCD**
- ⚡ Frame skipping (1 out of every 4–5 frames) to ensure smooth performance
- 🔒 No internet connection required — **runs fully offline**

---

## 🛠️ Tech Stack

| Component            | Details                                             |
|----------------------|------------------------------------------------------|
| **Hardware**         | Raspberry Pi 5, USB webcam, 2x16 I2C LCD            |
| **Language**         | Python 3                                            |
| **Libraries**        | `OpenCV`, `Scikit-learn`, `smbus2`, `pickle`, `numpy` |
| **Model**            | Classical ML (e.g., SVM or Random Forest), serialized via `pickle` |
| **Dataset**          | [Kaggle ASL Alphabet Dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet) |

---

## 🖼️ Demo

![Insert a GIF or image here of the system detecting a gesture and displaying it on the LCD]

---

## 📦 Installation

> ⚠️ This project assumes you already have Python and OpenCV installed on your Raspberry Pi.

1. **Clone the repo:**

```bash
git clone https://github.com/your-username/sign-language-pi.git
cd sign-language-pi
