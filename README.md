# CLIP-Distilled ShuffleNetV2 for Efficient Image Captioning

Ultra-efficient image captioning using knowledge distillation from CLIP, optimized for low-compute edge deployment.

---

## 📌 Overview
This project implements an end-to-end image captioning pipeline focused on the **efficiency–accuracy trade-off**.  
A powerful vision–language model (**CLIP ViT-B/32**) is used as a **teacher**, and its semantic knowledge is distilled into a lightweight **ShuffleNetV2-based student model**, enabling real-time image captioning on resource-constrained devices.

The system achieves **competitive captioning quality** while operating at **sub-0.2 GFLOPs**, making it suitable for mobile and IoT applications.

---

## 🧠 Key Concepts
- Knowledge Distillation (Teacher–Student Learning)
- Lightweight CNNs for Edge AI
- Vision–Language Modeling
- Attention-based Sequence Generation
- Model Compression & Efficiency Analysis

---

## 📂 Dataset
- **Flickr30k**
  - 31,783 images
  - 5 human-annotated captions per image
  - Train / Validation / Test split used

---

## 🏗️ Architecture
- **Teacher:** CLIP ViT-B/32 (pretrained vision–language model)
- **Student Encoder:** ShuffleNetV2 (2.04M parameters)
- **Decoder:** LSTM with spatial attention
- **Distillation Strategy:**
  - Feature-level distillation (MSE loss)
  - Task-level distillation (Cross-Entropy loss)
  - Weighted dual-loss optimization

---

## 📊 Evaluation Metrics
The model is evaluated using standard image captioning metrics:
- BLEU-1 / BLEU-4  
- METEOR  
- ROUGE-L  
- CIDEr  
- SPICE  

**Result Highlight:**  
- BLEU-4: **18.27%**  
- Encoder complexity: **0.192 GFLOPs**  
- ~95% parameter reduction vs teacher model

---

## ⚡ Efficiency & Deployment Readiness
- Sub-0.2 GFLOP encoder
- <1 ms estimated inference latency
- ~0.024 mJ per image
- Suitable for real-time edge and mobile deployment

---

## 📁 Repository Structure
.
├── notebook/
│ └── image_captioning.ipynb
├── report/
│ └── CLIP_Distilled_ShuffleNetV2.pdf
├── requirements.txt
└── README.md


---

## 🚀 How to Use
1. Clone the repository
2. Install dependencies from `requirements.txt`
3. Open the Jupyter notebook inside the `notebook/` folder
4. Run cells sequentially to train and evaluate the model

---

## 🔮 Future Work
- Scaling experiments to larger datasets (e.g., MS-COCO)
- Post-training quantization (INT8 / FP16)
- Faster or transformer-based lightweight decoders

---

## 👤 Author
**Agnik Patra**  
B.Tech CSE (AIML), VIT Vellore  

---

## 📎 Note
This repository is intended as a **project demonstration** for learning and experimentation in efficient deep learning and image captioning.


## 📁 Repository Struc
