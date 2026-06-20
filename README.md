# ✍️ Handwritten Digits Classification — Model Comparison

Comparing **3 machine learning models** on handwritten digit recognition (0-9) using 8x8 pixel images — SVM achieves the highest accuracy at **97.5%**.

---

## 🎯 Problem Statement

Given 8x8 pixel grayscale images of handwritten digits, classify each image as one of 10 digits (0–9).

- **Dataset**: Scikit-learn Digits Dataset
- **Samples**: 1,797 images, 64 pixel features
- **Classes**: 10 (digits 0–9)
- **Train/Test split**: 80/20

---

## 🏆 Model Comparison Results

| Model | Accuracy | CV Average (5-fold) |
|-------|----------|---------------------|
| **SVM (linear, C=1)** | **97.50%** | 97.01% |
| Random Forest (n=100) | 97.22% | 97.49% |
| Decision Tree | 84.17% | 85.04% |

**Winner: SVM** with 97.5% accuracy ✅

---

## 🔄 ML Pipeline (same for all models)

### 1. EDA & Visualization
- Target class distribution (balanced ~180 per digit)
- Display of first 10 handwritten digit images
- Pixel value distribution histograms (64 features)
- Correlation heatmap

### 2. Preprocessing
- 80/20 train/test split
- StandardScaler normalization

### 3. Evaluation Metrics
- Accuracy Score
- Confusion Matrix
- Classification Report (Precision, Recall, F1)
- 5-Fold Cross Validation

---

## 📊 Detailed Results

### 🥇 SVM — Linear Kernel (Best Model)
```
Accuracy       : 97.50%
CV Average     : 97.01%
kernel         : linear
C              : 1
```

### 🥈 Random Forest
```
Accuracy       : 97.22%
CV Average     : 97.49%
n_estimators   : 100
random_state   : 42
```

### 🥉 Decision Tree
```
Accuracy       : 84.17%
CV Average     : 85.04%
random_state   : 42
```

### Key Insight
Decision Tree underperforms because it creates rigid boundaries that don't generalize well on high-dimensional pixel data (64 features). SVM and Random Forest handle high dimensions much better.

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python |
| Data Analysis | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| ML Models | Scikit-learn (SVM, RandomForest, DecisionTree) |
| Evaluation | Confusion Matrix, Classification Report, Cross-Validation |
| Preprocessing | StandardScaler |

---

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Run notebooks in order:
1. `digits_SVM_week4_2.ipynb` — SVM model
2. `digits_randomforest_classifier_week5_2.ipynb` — Random Forest
3. `digits_decision_classifier_week5_1.ipynb` — Decision Tree

> Dataset loaded from `sklearn.datasets.load_digits()` — no download needed.

---

## 📁 Project Structure

```
handwritten-digits-classification/
│
├── digits_SVM_week4_2.ipynb                      # SVM — 97.5%
├── digits_randomforest_classifier_week5_2.ipynb  # Random Forest — 97.2%
├── digits_decision_classifier_week5_1.ipynb      # Decision Tree — 84.2%
└── README.md
```

---

## 👩‍💻 Author

**Angela** — Data Scientist | AI • ML • GenAI • RAG  
📍 Kuala Lumpur, Malaysia  
🔗 [GitHub](https://github.com/angelaadida)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
