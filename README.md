# CardBlur
# Privacy-Preserving Card Detection and Blurring

This repository is based on our capstone project at **Prince Mohammad Bin Fahd University – NITA AI Practitioner Diploma**.  
The project addresses privacy and security risks associated with the unintentional exposure of sensitive personal information, such as ID cards and passports, in images and video feeds.

---

## 📖 Overview
Sensitive documents are often captured through webcams, mobile devices, and surveillance systems, creating risks like **identity theft** and **unauthorized access**.  
Our solution introduces a **real-time system** that detects and automatically blurs sensitive regions (faces, ID text, and card areas) to safeguard privacy.

---

## 🔍 Objectives
- **Accurate Detection:** Identify sensitive components including faces, card regions, and text.  
- **Automated Blurring:** Apply consistent, reliable blurring without manual edits.  
- **Real-Time Processing:** Support both static images and live video streams.  
- **Robustness:** Handle diverse document types and challenging environments (e.g., hand-held IDs, noisy backgrounds).  

---

## 🧠 Methodology
- **Dataset:**  
  - *TrialforGeneratedIDs* dataset (3,000 images, 10 document types).  
  - Additional Saudi ID samples for local relevance.  
  - Custom hand-crafted images with cards in hand across varied backgrounds.  

- **Preprocessing:**  
  - Conversion of annotations into YOLO format.  
  - Bounding box verification and dataset balancing.  

- **Model:**  
  - **YOLOv8s** (You Only Look Once).  
  - Multiple progressive training stages to improve generalization.  
  - Achieved strong performance with precision and recall above 95% in final stage.

---

## 🖼️ Dataset Samples

<div align="center">
  <img src="srb_passport_rot_75.jpg" alt="Serbia passport sample (rotated)" width="30%"/>
  <img src="fin_id_rot_53.jpg" alt="Finland ID sample (rotated)" width="30%"/>
  <img src="saudi_id_06.jpg" alt="Saudi ID sample" width="30%"/>
</div>

---

## 📊 Key Results
| Training Stage | mAP50 | mAP50-95 | Recall | Precision |
|----------------|-------|----------|--------|-----------|
| Stage 1        | 0.89  | 0.79     | 0.86   | 0.92      |
| Stage 2        | 0.93  | 0.84     | 0.90   | 0.94      |
| Stage 3        | 0.94  | 0.86     | 0.92   | 0.93      |
| Stage 4        | 0.96  | 0.92     | 0.95   | 0.98      |

The model demonstrated **robust detection across multiple ID types**, improving especially in challenging scenarios like hand-held cards and diverse backgrounds.

---

## 🌍 Applications
- **Security systems** (airports, banks, government offices)  
- **Remote work environments** (document verification in video calls)  
- **Public platforms** (sharing images/videos without exposing personal data)  

---

## ⚠️ Ethical Considerations
- Designed for **privacy preservation**, not surveillance.  
- Users must comply with **data protection laws** and ensure **ethical deployment**.  

---

## 👩‍💻 Team
- **Project Manager:** Renad Almutairi  
- **Data Specialist:** Jory Alsultan  
- **Machine Learning:** Shatha Khawaji  
- **Web & Deployment:** Yara Alsardi  

---

## 📄 Citation
If you use this work in research or industry, please cite:

