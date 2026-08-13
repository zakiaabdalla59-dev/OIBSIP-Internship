# Task 4: Email Spam Detection with Machine Learning

## 📌 Overview
Email and SMS spam filtering is a fundamental application of **Natural Language Processing (NLP)** and supervised text classification. This project builds an automated end-to-end pipeline to preprocess raw message text, convert terms into numerical TF-IDF feature vectors, and classify messages as either **Ham** (Legitimate) or **Spam** (Unsolicited/Malicious).

---

## 📂 Files Included
- `Email_Spam_Detection.ipynb`: Fully executed Jupyter Notebook detailing text preprocessing, feature vectorization, model training, metric evaluation, and critical analysis.
- `spam.csv`: SMS / Email Spam Collection dataset (1,000 records).
- `README.md`: Project summary, model metrics, and recall analysis.

---

## 🔬 NLP Pipeline & Methodology
1. **Exploratory Data Analysis**:
   - Checked class balance (75% Ham, 25% Spam).
   - Engineered `Message_Length` and `Word_Count` features.
   - Identified character length differences between ham and spam.
2. **Text Preprocessing (`clean_text`)**:
   - Lowercasing text.
   - Removing special characters, numbers, and punctuation using Regex (`re.sub(r'[^a-zA-Z\s]', '', text)`).
   - Removing English stop words using NLTK (`stopwords.words('english')`).
   - Normalizing word roots using NLTK **Porter Stemmer**.
3. **TF-IDF Feature Extraction**:
   - `TfidfVectorizer(max_features=3000, ngram_range=(1, 2))`.
4. **Machine Learning Classifiers**:
   - Multinomial Naive Bayes (`MultinomialNB(alpha=0.1)`).
   - Logistic Regression.
   - Support Vector Machine (`SVC(kernel='linear')`).
   - Random Forest Classifier.

---

## 📊 Benchmark Evaluation Results

| Classifier Model | Accuracy | Precision (Spam) | Recall (Spam) | F1-Score (Spam) |
|---|---|---|---|---|
| **Multinomial Naive Bayes** | **100.0%** | **1.0000** | **1.0000** | **1.0000** |
| **Support Vector Machine** | **100.0%** | **1.0000** | **1.0000** | **1.0000** |
| **Logistic Regression** | **99.5%** | **1.0000** | **0.9800** | **0.9899** |
| **Random Forest** | **99.5%** | **1.0000** | **0.9800** | **0.9899** |

---

## ⚠️ Why Precision & Recall are Critical in Spam Detection

1. **False Positives (FP) & High Precision**:
   - **Scenario:** A legitimate email (**Ham**) is misclassified as **Spam** and sent to junk folder.
   - **Risk:** User misses crucial communication (e.g., job offer, verification code).
   - **Solution:** **High Precision** ensures zero valid emails are lost to the spam folder.

2. **False Negatives (FN) & High Recall**:
   - **Scenario:** A phishing email (**Spam**) is misclassified as **Ham** and delivered to the inbox.
   - **Risk:** Security vulnerability, malware infection, and phishing scams.
   - **Solution:** **High Recall** ensures maximum spam removal from the inbox.

---
*Completed for Oasis Infobyte Data Science Internship (OIBSIP)*
