# 🌿 Self-Supervised Crop Disease Detection using SimCLR (Low-Label Learning)

## 📌 Project Overview
In real-world agriculture, collecting crop leaf images is easy, but labeling them with correct disease categories is expensive and requires expert knowledge. Traditional supervised deep learning models perform poorly when labeled data is limited.

This project solves the problem using **Self-Supervised Learning (SimCLR)**:

✅ Pretrain a CNN encoder on **unlabeled leaf images**  
✅ Fine-tune the pretrained encoder using only **10% labeled data**  
✅ Achieve high accuracy even under low-label settings  

---

## 🚀 Key Innovation
Instead of directly training a classifier from scratch, we use **SimCLR contrastive learning** to learn strong leaf representations without needing labels.

This makes the system highly suitable for:

- Low-resource agricultural environments  
- Real-world farming scenarios  
- Rare crop disease detection tasks  

---

## 🧠 Methodology

### ✅ Phase 1: Self-Supervised Pretraining (SimCLR)

- Generate two augmented views of the same leaf image
- Train the encoder using contrastive loss
- Learn meaningful features such as:
  - texture patterns  
  - disease spots  
  - leaf structure  

  
---

### ✅ Phase 2: Fine-Tuning with Limited Labels

- Freeze the pretrained encoder
- Train only a lightweight classifier head
- Use only **10% labeled disease data**


---

## 📂 Dataset Used
We used a balanced subset of the **PlantVillage Dataset** consisting of 5 classes:

- Tomato_Late_blight  
- Tomato_Leaf_Mold  
- Tomato_healthy  
- Potato___Early_blight  
- Pepper__bell___healthy  

Total Images Used: **6930**

---

## 🔥 Results

### ✅ Comparison: Supervised vs Self-Supervised Learning

| Model Type | Labels Used | Validation Accuracy |
|-----------|------------|---------------------|
| Supervised ResNet18 (Scratch) | 10% | **35.91%** ❌ |
| SimCLR SSL + Fine-Tuning | 10% | **95.27%** ✅ |

---

## 📊 Conclusion
This experiment clearly proves that:

✅ Self-Supervised Learning drastically reduces dependency on labeled agricultural datasets  
✅ SSL models generalize much better under low-data settings  
✅ SimCLR is a powerful approach for crop disease detection

---

## 🛠 Tech Stack

- Python  
- PyTorch  
- Torchvision  
- SimCLR Contrastive Learning  
- PlantVillage Dataset  
- Google Colab GPU Training  

---
Future Improvements
1. Expand to all 15 PlantVillage disease classes
2. Deploy as a Streamlit Web App for farmers
3. Add Explainable AI (Grad-CAM heatmaps)
4. Try advanced SSL methods like BYOL, MoCo, MAE

Acknowledgments
1. PlantVillage Dataset (Kaggle)
2. SimCLR Paper: A Simple Framework for Contrastive Learning of Visual Representations
3. PyTorch Community


