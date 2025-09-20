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
  - Progressive training with background diversification and hand-held cases.

---

## 🖼️ Dataset Samples

<div align="center">

<img src="https://github.com/user-attachments/assets/23803715-7971-4bbc-980f-b7d487da4df4" alt="saudi_id_06" width="45%"/>
<img src="https://github.com/user-attachments/assets/7bdf24e1-c89b-455b-8c12-0db2f5d7d867" alt="fin_id_rot_89" width="45%"/>
<img src="https://github.com/user-attachments/assets/32d60923-a238-4321-89ce-720d3398f068" alt="rus_internalpassport_rot_32" width="45%"/>
<img src="https://github.com/user-attachments/assets/760de171-8208-4cd7-96e6-520e48eacd98" alt="srb_passport_rot_47" width="45%"/>

</div>

---

## 📊 Key Results

| Training Stage | mAP50  | Train Box Loss | Val Box Loss |
|----------------|--------|----------------|--------------|
| Stage 1        | 0.9326 | 0.7288         | 0.8372       |
| Stage 2        | 0.9455 | 0.8515         | 0.9461       |
| Stage 3        | 0.9660 | 0.8587         | 0.6099       |

These stages reflect improvements from adding diverse backgrounds and targeting hand-held card scenarios.

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

