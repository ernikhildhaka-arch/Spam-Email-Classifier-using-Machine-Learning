# 📧 Spam Email Classifier using Machine Learning

A machine learning project that classifies emails as **Spam** or **Ham (Not Spam)** using Natural Language Processing (NLP) techniques and Scikit-learn.

---

## 🚀 Project Overview

This project builds a spam email classifier using the **Apache SpamAssassin Public Dataset**. The emails are preprocessed, converted into numerical feature vectors, and classified using different machine learning algorithms.

The project compares multiple feature extraction techniques and classifiers to identify the best-performing model.

---

## 📂 Dataset

The dataset is taken from the **Apache SpamAssassin Public Corpus**.

### Ham Emails
- Easy Ham
- Easy Ham 2
- Hard Ham

### Spam Emails
- Spam
- Spam 2

Labels:

- **0 → Ham (Legitimate Email)**
- **1 → Spam**

---

## 📁 Project Structure

```
Spam_Classifier/
│
├── data/
│   ├── 20030228_easy_ham/
│   ├── 20030228_easy_ham_2/
│   ├── 20030228_hard_ham/
│   ├── 20030228_spam/
│   └── 20030228_spam_2/
│
├── notebooks/
│   └── Spam_Classifier.ipynb
│
├── models/
│   ├── spam_classifier.pkl
│   └── tfidf_vectorizer.pkl
│
├── README.md

```

---

## ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Joblib
- Regular Expressions (re)
- Jupyter Notebook

---

## 🛠 Workflow

### 1. Load Dataset

- Read every email from the dataset folders.
- Combine ham folders into one dataset.
- Combine spam folders into one dataset.

---

### 2. Create Labels

```
Ham  → 0
Spam → 1
```

---

### 3. Train-Test Split

Split the dataset into:

- Training Set
- Testing Set

using Scikit-learn's `train_test_split()`.

---

### 4. Email Preprocessing

Each email undergoes preprocessing:

- Convert to lowercase
- Remove punctuation
- Replace URLs with `URL`
- Replace numbers with `NUMBER`
- Remove unnecessary characters
- Normalize whitespace

---

### 5. Feature Extraction

Two feature extraction techniques were used.

### CountVectorizer

Converts each email into a vector containing the frequency of each word.

Example:

```
Free Free Offer

↓

[2,1]
```

---

### TF-IDF Vectorizer

Assigns weights to words based on their importance in the entire dataset.

Common words receive lower weights, while informative words receive higher weights.

---

## 🤖 Machine Learning Models

The following classifiers were trained and compared.

- Multinomial Naive Bayes
- Logistic Regression

Both models were evaluated using CountVectorizer and TF-IDF Vectorizer.

---

## 📊 Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

---


## 💾 Model Saving

The trained model and TF-IDF vectorizer are saved using **Joblib**.

```
spam_classifier.pkl

tfidf_vectorizer.pkl
```

This allows the model to be loaded later without retraining.

---

## ✉️ Example Prediction

Input:

```
Congratulations!

You have won ₹50,000.

Click here to claim your prize.
```

Output:

```
Spam
```

---

Input:

```
Hi,

Let's meet tomorrow to discuss the machine learning project.

Thanks.
```

Output:

```
Ham
```

---

## 📚 Key Concepts Learned

- Text preprocessing
- Natural Language Processing (NLP)
- Feature extraction
- CountVectorizer
- TF-IDF Vectorizer
- Machine Learning Classification
- Model Evaluation
- Model Serialization with Joblib

---

## 🎯 Future Improvements

- Add stemming and lemmatization
- Remove stopwords
- Hyperparameter tuning using GridSearchCV
- Try Linear SVM and Random Forest
- Deploy the model using Flask or FastAPI
- Build a web interface for real-time spam detection

---

## 📖 References

- Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow (Aurélien Géron)
- Apache SpamAssassin Public Corpus
- Scikit-learn Documentation

---

## 👨‍💻 Author

**Nikhil Dhaka**

Machine Learning & Data Science Enthusiast

Currently learning:
- Machine Learning
- Deep Learning
- Computer Vision
- Natural Language Processing

---

⭐ If you found this project helpful, consider giving it a star!
