# 🚀 Secure Data Hiding via Panoptic Segmentation

A novel **segmentation-aware steganography system** that leverages deep learning-based panoptic segmentation to embed encrypted data within semantically meaningful regions of an image.

---

## 📌 Overview

Traditional steganography techniques (e.g., LSB) embed data sequentially across pixels, making them vulnerable to detection.  
This project introduces a **context-aware data hiding approach** using DETR (DEtection TRansformer), enabling intelligent selection of image regions for embedding.

> 💡 Idea: Hide data where it makes the most sense — not just anywhere.

---

## ⚙️ Key Features

- 🔍 **Panoptic Segmentation (DETR + ResNet-101)** identifies semantically meaningful regions in images.  
- 🧠 **Smart Region Selection** selects optimal embedding areas based on pixel density and segmentation masks.  
- 🔐 **AES-256 Encryption** encrypts payload before embedding for enhanced security.  
- 🧩 **Prime-based LSB Embedding** uses Sieve of Eratosthenes for non-sequential embedding.  
- 🔁 **End-to-End Encode–Decode Pipeline** ensures accurate recovery of hidden messages.  

---

## 🏗️ Pipeline

Cover Image  
↓  
Panoptic Segmentation (DETR - ResNet-101)  
↓  
Semantic Region Selection (High-density segment)  
↓  
Message → AES-256 Encryption  
↓  
Prime-indexed LSB Embedding  
↓  
Stego Image  
↓  
(Decoding)  
↓  
Re-segmentation → Region Alignment  
↓  
LSB Extraction (Prime positions)  
↓  
AES Decryption → Original Message  

---

## 🛠️ Tech Stack

- **Language:** Python  
- **Deep Learning:** PyTorch, Torchvision  
- **Model:** DETR (ResNet-101 backbone)  
- **Image Processing:** OpenCV, NumPy  
- **Security:** AES-256 Encryption  
- **Dataset:** COCO 2017  

---

## 📊 Why This Approach?

| Method | Limitation |
|------|----------|
| Traditional LSB | Sequential embedding → easy detection |
| Random LSB | Less structured, still detectable |
| **This Work** | Context-aware + encrypted + non-sequential |

✅ Improves:
- Stealth  
- Robustness  
- Security  

---

## 📷 Example Workflow

1. Input an image  
2. Perform panoptic segmentation  
3. Select optimal embedding region  
4. Encrypt and embed message  
5. Generate visually indistinguishable stego-image  


---

