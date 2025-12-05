# 🧪 MedFuzz-Adversarial-Robustness

### Robustness Testing of Medical LLMs

Extended MedFuzz framework with novel adversarial perturbation strategies for medical LLM robustness testing.

---

## 🔬 Overview

This project addresses a critical safety gap in clinical AI by extending the **MedFuzz adversarial testing framework**. We introduce **three novel perturbation strategies**—numerical manipulation, medical terminology swapping, and treatment confusion—to evaluate the robustness of the **Llama-3.1-8b** model.

**Base Paper:** *MedFuzz: Exploring the Robustness of Large Language Models in Medical Question Answering*

---

## ✨ Key Results Summary

| **Metric**                | **Value**                                        |
| ------------------------- | ------------------------------------------------ |
| Overall Robustness Score  | **96.7%**                                        |
| Attack Success Rate (ASR) | **3.3%** (1 out of 30 perturbations)             |
| Primary Vulnerability     | **Medical Terminology Swap** (6.7% success rate) |
| Perfect Robustness        | **100%** against numerical manipulation          |

---

## 🧩 Novel Contributions

We introduced three new perturbation types designed to test clinical reasoning limitations:

### **1. Numerical Manipulation**

Alters clinical values (age, lab results, vital signs) by 10–30% to test holistic reasoning vs. threshold-based rules.

### **2. Medical Terminology Swap**

Replaces medical terms with similar-sounding conditions
*(e.g., “atrial fibrillation” → “atrial flutter”)*
to test semantic disambiguation.

### **3. Treatment Confusion**

Introduces plausible but incorrect treatment options to test model focus on the correct diagnostic pathway.

---

## 🎯 Key Findings

| **Status**                     | **Finding**                                                                  | **Insight**                                                   |
| ------------------------------ | ---------------------------------------------------------------------------- | ------------------------------------------------------------- |
| ✅ Perfect Numerical Robustness | Model achieved **100% robustness** against numerical manipulation.           | Indicates strong holistic clinical reasoning.                 |
| ⚠️ Terminology Vulnerability   | Medical terminology swap caused **6.7% attack success**.                     | Reveals semantic confusion — a key risk in clinical settings. |
| 🎯 High Overall Reliability    | **96.7% total robustness**, outperforming many models from original MedFuzz. | Confirms Llama-3.1-8b’s excellent baseline reasoning.         |

---

## 📊 Detailed Performance Metrics

### **Overall Performance**

| Metric              | Value |
| ------------------- | ----- |
| Questions Tested    | 15    |
| Total Perturbations | 30    |
| Successful Attacks  | 1     |
| Attack Success Rate | 3.3%  |
| Robustness Score    | 96.7% |

### **By Perturbation Type**

| Perturbation             | Success Rate | Robustness |
| ------------------------ | ------------ | ---------- |
| Medical Terminology Swap | 6.7%         | 93.3%      |
| Numerical Manipulation   | 0.0%         | 100.0%     |

---

## 🛠️ QUICK START: Replication Instructions

This project requires Python, standard scientific libraries, and access to the **Groq API** for running the Llama-3.1-8b model.

### **Prerequisites**

#### Install Dependencies

```bash
# Install scientific and API libraries
pip install groq pandas numpy matplotlib seaborn tqdm scipy
```

#### Get Groq API Key

Create an account and obtain your key from:
[https://console.groq.com](https://console.groq.com)

---

## ▶️ Running the Code (Google Colab Recommended)

1. Clone this repository OR upload the notebook.
2. Open **Innovation_Code.ipynb**.
3. Update your API key:

```python
groq_api_key = "YOUR_API_KEY_HERE"
```

4. Run all cells (**Runtime → Run all**).
5. Total execution time: **12–15 minutes**.
6. View robustness metrics in the output or in the `/results` folder.

---

## 👤 Author

**Muhammad Ghufran (25K-7615)**
