# ✍️ Handwritten Digits Classification — Random Forest

Image classification project using **Random Forest** to recognize handwritten digits (0-9) from 8x8 pixel images — achieving **97.2% accuracy**.

---

## 🎯 Problem Statement

Given 8x8 pixel grayscale images of handwritten digits, classify each image as one of 10 digits (0–9).

- **Dataset**: Scikit-learn Digits Dataset
- **Samples**: 1,797 images, 64 features (pixel values)
- **Classes**: 10 (digits 0–9)
- **Train/Test split**: 80/20

---

## 🔄 ML Pipeline

### 1. EDA & Visualization
- Target distribution (balanced classes ~180 per digit)
- Visual display of first 10 handwritten digit images
- Pixel value distribution histograms (64 features)
- Correlation heatmap of pixel features

### 2. Preprocessing
- StandardScaler normalization on pixel values
- No missing values in dataset

### 3. Model: Random Forest Classifier
```
Parameters:
  n_estimators : 100
  random_state : 42
```

---

## 🏆 Results

| Metric | Score |
|--------|-------|
| **Accuracy** | **97.22%** |
| Cross-val Average (5-fold) | **97.49%** |

### Classification Report

| Digit | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| 0 | 1.00 | 0.97 | 0.98 |
| 1 | 0.97 | 1.00 | 0.98 |
| 2 | 1.00 | 1.00 | 1.00 |
| 3 | 1.00 | 0.94 | 0.97 |
| 4 | 0.98 | 1.00 | 0.99 |
| 5 | 0.94 | 0.96 | 0.95 |
| 6 | 0.97 | 0.97 | 0.97 |
| 7 | 0.97 | 0.97 | 0.97 |
| 8 | 0.97 | 0.97 | 0.97 |
| 9 | 0.95 | 0.95 | 0.95 |
| **avg** | **0.97** | **0.97** | **0.97** |

### Confusion Matrix
```
[[32  0  0  0  1  0  0  0  0  0]
 [ 0 28  0  0  0  0  0  0  0  0]
 [ 0  0 33  0  0  0  0  0  0  0]
 [ 0  0  0 32  0  1  0  0  1  0]
 [ 0  0  0  0 46  0  0  0  0  0]
 [ 0  0  0  0  0 45  1  0  0  1]
 [ 0  0  0  0  0  1 34  0  0  0]
 [ 0  0  0  0  0  0  0 33  0  1]
 [ 0  1  0  0  0  0  0  0 29  0]
 [ 0  0  0  0  0  1  0  1  0 38]]
```

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python |
| Data Analysis | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| ML Model | Scikit-learn (RandomForestClassifier) |
| Evaluation | Confusion Matrix, Classification Report, Cross-Validation |
| Preprocessing | StandardScaler |

---

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Open `digits_randomforest_classifier_week5_2.ipynb` in Jupyter Notebook and run all cells.

> Dataset is loaded directly from `sklearn.datasets.load_digits()` — no download needed.

---

## 📁 Project Structure

```
handwritten-digits-classification/
│
├── digits_randomforest_classifier_week5_2.ipynb   # Main notebook
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
