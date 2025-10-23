# 🫁 Pneumonia Detection (Colab + Django + VGG19 + TensorFlow)

---

### 🔗 Links

- **All Models (Drive):** <a href="https://drive.google.com/drive/folders/1U46EsIHwJhOGTT6QQvoPfhkrfDRHd1Iw?usp=sharing" target="_blank">Google Drive</a>  
- **Dataset Used:** <a href="https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia" target="_blank">Paul Mooney (Kaggle)</a>  
- **Website Repository:** <a href="https://github.com/AsteroidCap4040/Pneumonia-Detection-Django" target="_blank">GitHub - Pneumonia Detection Website</a>

---

### 🧬 Dataset Summary

| Dataset Type | Normal Images | Pneumonia Images |
|---------------|---------------|------------------|
| Training      | 1341          | 3875             |
| Validation    | 8             | 8                |
| Testing       | 234           | 390              |

---

### 💻 About This Colab File

This Colab notebook contains all **models and code** written for my **Pneumonia Detection Website**.  
The website has **two detection modes**:

---

## 🩺 1. Single Detection Mode

Upload your **Chest X-ray**, and the model detects **whether you have Pneumonia or not**.

**🧠 Models Trained (30 Epochs Each):**

| Model            | Accuracy | Notes |
|------------------|-----------|-------|
| **VGG-19**       | 91.67%    | ✅ Considered the best for X-ray related ML |
| **ResNet152**    | 73.88%    | - |
| **DenseNet121**  | 90.38%    | - |
| **EfficientNet-B3** | 62.50% | ⚠️ Early Stopping |

➡️ **VGG-19** was chosen for the final deployment due to its superior performance on X-ray data.

---

## 📈 2. Multi Detection Mode

Upload **multiple X-rays** (with dates), and the system generates a **graph** showing the **increase/decrease in Pneumonia infection** over time.

**⚠️ Issue Encountered:**  
The system initially misinterpreted the **shadowed areas outside the lungs** as infection zones, inflating the infection percentage.

**🧩 Fix Implemented:**  
To counter this, I calculated the **average shadowed pixels** from **healthy lung X-rays** and subtracted that from the Pneumonia images.  
Not a perfect solution, but it produced **satisfactory and believable results**.

---

## 😤 Final Thoughts

### **F*** MEDICAL-RELATED DATASETS!!!**  
Why the fuck are they so *sparse and inconsistent,* and an absolute pain to work with.

---

