# 📩 SMS Spam Detection — Hybrid TF-IDF + Logistic Regression

A production-style machine learning project that classifies SMS messages as **Spam** or **Ham (legitimate)** using a hybrid feature engineering approach and an optimized Logistic Regression model.

Built with a focus on **accuracy, robustness, and deployment readiness**, this system is resilient against slang, typos, and intentional misspellings commonly used in spam messages.

---

## 🚀 Project Highlights

✅ **~99.46% Accuracy** on the test dataset
✅ **Zero false positives** — legitimate messages were never flagged as spam
✅ Detects **143 / 149 spam messages** successfully
✅ Hybrid NLP pipeline improves real-world reliability
✅ Interactive **Gradio web interface** included
✅ Fully reproducible with pinned dependencies

---

## 🧠 How It Works

### 🔹 Hybrid Feature Engineering

Instead of relying only on word tokens, this project combines:

* **Word N-grams (1–2)** → captures semantic meaning
* **Character N-grams (2–5)** → detects obfuscated spam like:

FREE!!!
Fr33!!!
F.r.e.e

This dramatically improves robustness in noisy text environments.

Implemented using **Scikit-Learn's `FeatureUnion`**.

---

### 🔹 Model Optimization

The classifier was tuned to perform reliably on an imbalanced dataset.

**Techniques Used:**

* Logistic Regression with **C = 10.0**
* `class_weight="balanced"` to prevent bias toward majority class
* Increased iteration cap for convergence

---

## 📊 Performance Metrics

| Metric                | Score          |
| --------------------- | -------------- |
| **Accuracy**          | **~99.46%**    |
| **Ham Precision**     | **100%**       |
| **Spam Recall**       | **96%**        |
| **Confidence Scores** | Often **>99%** |

👉 The model prioritizes **not flagging real messages**, making it suitable for production filtering systems.

---

## 🛠 Tech Stack

**Machine Learning:**
Python, Scikit-Learn, TF-IDF, Logistic Regression

**Visualization:**
Matplotlib, Seaborn

**Interface:**
Gradio

**Utilities:**
NumPy, Pandas, Joblib

---

## 📦 Dataset

**UCI SMS Spam Collection**

* 5,500+ labeled SMS messages
* Real-world dataset commonly used for NLP benchmarking

The dataset is automatically downloaded in the notebook.

---

## ⚙️ Installation & Usage

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/<your-username>/sms-spam-detector.git
cd sms-spam-detector
```

---

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 3️⃣ Run the Notebook

Open:

```
sms_spam_detector.ipynb
```

Run all cells to:

✅ Train the model
✅ Evaluate performance
✅ Visualize confusion matrix
✅ Launch the Gradio interface

---

## 🧪 Example Predictions

**Spam Message:**

> "WINNER!! You have been selected for a £900 prize!"

✅ Predicted: **Spam**
✅ Confidence: **Very High**

---

**Normal Message:**

> "Hey, are we still meeting for dinner tonight?"

✅ Predicted: **Ham**
✅ Confidence: **Very High**

---

## 🔒 System Stability

To prevent runtime conflicts:

* All critical dependencies are version-pinned
* Compatible versions of **Scikit-Learn, Pillow, and Gradio** are enforced
* The environment is designed to be reproducible

---

## 💡 Future Improvements

🔹 Analyze the **6 missed spam messages** to identify new predictive features
🔹 Add engineered signals such as:

* message length
* special character frequency
* URL / phone number detection

🔹 Export the trained pipeline with **Joblib** for production use
🔹 Deploy as a REST API or web service

---

## 🎯 Skills Demonstrated

* End-to-end ML pipeline development
* Advanced feature engineering
* Handling imbalanced datasets
* Model tuning & evaluation
* Interactive ML app development
* Production-oriented thinking

---

## ⭐ Why This Project Matters

Spam detection is a real-world NLP challenge used in:

* Messaging platforms
* Email providers
* Fraud detection systems
* Telecom infrastructure

This project demonstrates the ability to build **reliable, high-accuracy ML systems ready for deployment.**

---

⭐ If you found this project useful, consider starring the repository!
