# Phishing Email Detection with Explainable AI (XAI)

This project focuses on detecting phishing emails using Natural Language Processing (NLP) techniques and interpretable machine learning models. It combines traditional classification algorithms with explainability tools such as SHAP and LIME to ensure transparency and insight into how decisions are made.

---

## 📁 Dataset

The dataset (`Phishing_Email.csv`) contains email messages labeled as either:

- `1` — Phishing email  
- `0` — Legitimate email

### Column:
- `Email Text` — the body/content of the email.

---

## 🧹 Preprocessing

1. **Blank Removal**  
   Empty or whitespace-only rows are identified and removed.

2. **Text Normalization**
   - Tokenization and lowercasing
   - Removal of stopwords using NLTK
   - Lemmatization using `WordNetLemmatizer`
   - Custom preprocessing function applied to every email

---

## 🧪 Feature Engineering

### TF-IDF Vectorization

Text is converted into numerical vectors using **Term Frequency-Inverse Document Frequency**, which emphasizes important and unique terms in the corpus.


## 🤖 Models Used
Several machine learning models were trained and evaluated:

### Logistic Regression

### Naive Bayes

### Support Vector Machine (SVM)

### Random Forest

Each model was evaluated using:

Accuracy

Precision, Recall, F1-score (via classification_report)

## 🧠 Explainable AI (XAI)
To interpret and explain the model's predictions, two XAI frameworks were used:

### ✅ SHAP (SHapley Additive Explanations)
Provides global and local explanations for model behavior

SHAP summary plots highlight the most influential words in predictions

Waterfall plots show word-level contributions in individual emails
### ✅ LIME (Local Interpretable Model-Agnostic Explanations)
Explains model decisions per email

Useful to visualize which words led to a phishing or legit classification
## 📊 Key Results
SVM and Random Forest showed the best performance

Common phishing terms identified: “account”, “verify”, “login”, “suspend”, “click”

SHAP and LIME consistently highlighted relevant terms and boosted trust in the model


## 🎯 Project Goal
To develop a robust phishing email detection system that is not only accurate, but explainable. By incorporating XAI methods like SHAP and LIME, we aim to make machine learning decisions transparent and interpretable — a crucial step in security-focused applications.
