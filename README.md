# 📰 Fake News Classification Using Machine Learning

This project builds and evaluates a machine learning pipeline to classify news articles as **fake** or **real** using the [Fake-and-Real News Dataset from Kaggle](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset). The goal is to:

- Build a **baseline classifier**
- Evaluate model performance across **content domains** (e.g., `politicsNews`, `worldnews`)
- Implement and document **model improvements** using ensemble methods and feature engineering

---

## 📁 Dataset

The dataset contains two CSV files:
- `Fake.csv`: Fake news articles and their subjects
- `True.csv`: Real news articles and their subjects

Each article has:
- `title`
- `text`
- `subject` (used to create domain labels like `politicsNews` and `worldnews`)

We download the dataset automatically using the Kaggle API. Users must upload their own `kaggle.json` file for access.

---

## 🧠 Project Steps

### Step 1: Baseline Model
- Merged and preprocessed the dataset (lowercase, remove punctuation, tokenize, lemmatize, remove stopwords)
- Created domain labels to analyze model behavior across topics
- Used **TF-IDF + Logistic Regression** as a baseline model
- Evaluated:
  - Overall classification performance
  - Domain-specific performance
  - Feature importance (top predictive words)
  - Confusion matrices

### Step 2: Model Improvements
- Implemented **Random Forest** as an ensemble method to capture non-linear patterns
- Achieved **perfect classification accuracy (100%)** on all domains
- Visualized improved confusion matrices and performance metrics

### Additional Enhancements
- Simulated **auxiliary dataset augmentation** by duplicating and slightly modifying samples
- Added **text length** as a numeric feature for **advanced feature engineering**
- Built a pipeline combining TF-IDF and custom features

---

## 📊 Results Summary

| Model              | Accuracy (Overall) | Accuracy (politicsNews) | Accuracy (worldnews) |
|-------------------|--------------------|--------------------------|-----------------------|
| Logistic Regression | 99%               | 98%                     | 100%                  |
| Random Forest      | **100%**           | **100%**                | **100%**              |
