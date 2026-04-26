# 🧠 Comment Category Prediction

## 📌 Overview
This project focuses on building a machine learning model to predict the category assigned to user-generated comments on an online discussion platform. The dataset includes textual content along with metadata such as user engagement signals, symbolic indicators, and system-generated features.

The goal is to analyze these diverse features and develop a model capable of accurately classifying comments into predefined categories.

---

## 📊 Dataset Description
The dataset consists of three main files:

- **train.csv** → Contains features along with the target label  
- **test.csv** → Contains features without labels (used for prediction)  
- **sample_submission.csv** → Format for submitting predictions  

### 🔑 Features

- **comment** → Raw text content  
- **created_date** → Timestamp of comment  
- **post_id** → Thread identifier  
- **emoticon_1 / emoticon_2 / emoticon_3** → Symbol indicators  
- **upvote / downvote** → Engagement metrics  
- **if_1 / if_2** → Internal platform signals  
- **race / religion / gender / disability** → Topic indicators  
- **label** → Target variable (4 categories)

---

## ⚙️ Approach

### 🧹 Data Preprocessing
- Handled missing values (filled categorical with `"unknown"`)
- Converted text data to string format
- Extracted numerical and categorical features
- Standardized numeric features using scaling

### 🧠 Feature Engineering
- **TF-IDF Vectorization** (5000 features, uni + bi-grams)
- Combined text + numeric features using sparse matrices
- Created advanced features:
  - Engagement score (upvote - downvote)
  - Engagement ratio
  - Comment length & word count
  - Time-based features (hour, day of week)

---

## 🤖 Models Used

### Linear Models
- Logistic Regression  
- SGD Classifier  

### Traditional ML
- Naive Bayes  
- KNN  
- SVM  

### Ensemble Methods
- Random Forest  
- AdaBoost  
- Stacking Classifier  

### Neural Network
- MLP Classifier  

### 🚀 Final Model
- **LightGBM (Best Performing Model)**  

---

## 📈 Results

| Model                | Accuracy |
|---------------------|---------|
| Logistic Regression | ~0.90   |
| Random Forest       | ~0.91   |
| Stacking            | ~0.91   |
| MLP                 | ~0.90   |
| **LightGBM**        | **0.914** ✅ |

- Best validation accuracy: **91.4%**
- Demonstrates strong performance using combined text and engineered features

---

## 📊 Key Insights

- Text features (TF-IDF) are highly informative  
- Combining numeric + text features improves performance  
- Feature engineering significantly boosts accuracy  
- Ensemble models outperform basic classifiers  

---

## 🛠️ Tech Stack

- **Python**
- **Pandas, NumPy**
- **Scikit-learn**
- **LightGBM**
- **Matplotlib, Seaborn**

---

## 📁 Project Structure

