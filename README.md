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
| **Model**            | Classical ML (Random Forest), serialized via `pickle` |
| **Dataset**          | [Kaggle ASL Alphabet Dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet) |

---

## 🖼️ Demo
found on my linkedin profile
https://www.linkedin.com/feed/update/urn:li:activity:7323834655709769729/

---

⚡ Optimization Details

To ensure real-time performance on the Pi 5:
The system skips 3–4 frames between each prediction.
Only hand region is processed to reduce noise and input size.
Uses classical ML (e.g., SVM or RandomForest) instead of deep learning for lightweight inference.

🚧 Limitations & Future Work

Currently supports 28 static signs (no dynamic gestures or full sentences).
No AI accelerator used (yet) — planned upgrade for word and phrase recognition.
LCD displays one character at a time; future versions may support larger or scrolling displays.

---

huge thanks to :
@misc{akash_nagaraj_2018,
	title={ASL Alphabet},
	url={https://www.kaggle.com/dsv/29550},
	DOI={10.34740/KAGGLE/DSV/29550},
	publisher={Kaggle},
	author={Akash Nagaraj},
	year={2018}
}

