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

