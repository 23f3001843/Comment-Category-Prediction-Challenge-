# Comment Category Prediction

## Overview
This project focuses on building a machine learning model to predict the category assigned to user-generated comments on an online discussion platform. The dataset combines textual content with metadata such as engagement signals, symbolic indicators, and internal system features.

The objective is to leverage both text and structured data to accurately classify comments into one of four categories.

---

## Dataset

The dataset is hosted on Kaggle and is not included in this repository due to size constraints.

Download from: https://www.kaggle.com/competitions/comment-category-prediction-challenge

### Files:
- `train.csv` → Training data with labels  
- `test.csv` → Test data without labels  
- `sample_submission.csv` → Submission format  

After downloading, place the files in the same directory as the notebook.

---

## Approach

### Data Preprocessing
- Handled missing values (categorical → `"unknown"`, others → `0`)
- Converted text data to string format
- Separated text, numeric, and categorical features
- Applied scaling to numeric features

---

### Feature Engineering
- **TF-IDF Vectorization** (5000 features, unigrams + bigrams)
- Combined text and numeric features using sparse matrices
- Engineered additional features:
  - Engagement score (`upvote - downvote`)
  - Engagement ratio
  - Comment length and word count
  - Time-based features (hour, day of week)

---

## Models Implemented

- Logistic Regression  
- SGD Classifier  
- Naive Bayes  
- KNN  
- SVM  
- Random Forest  
- AdaBoost  
- Stacking Classifier  
- MLP Classifier  

---

## Final Model

**LightGBM (Best Performing Model)**  

- Validation Accuracy: **91.4%**  
- Achieved using advanced feature engineering + optimized hyperparameters  
- Demonstrated best performance among all tested models  

---

## Results Summary

| Model                | Accuracy |
|---------------------|---------|
| Logistic Regression | ~0.90   |
| Random Forest       | ~0.91   |
| Stacking            | ~0.91   |
| MLP                 | ~0.90   |
| **LightGBM**        | **0.914** |

---

## Key Insights

- Text features (TF-IDF) are highly informative  
- Combining structured + unstructured data improves performance  
- Feature engineering significantly boosts model accuracy  
- Ensemble models outperform simpler models  

---

## Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn  
- LightGBM  
- Matplotlib, Seaborn  

---

## Project Structure
```
comment-category-prediction/
├── 23f3001843-notebook-t12026.ipynb
└── README.md
```
---

## How to Run

1. Clone this repository  
2. Download dataset from Kaggle  
3. Place `.csv` files in the project folder  
4. Open and run the notebook: jupyter notebook


---

## Future Improvements

- Hyperparameter tuning for further optimization  
- Deep learning approaches (LSTM, Transformers)  
- Better handling of class imbalance  
- Use of advanced NLP techniques (word embeddings, BERT)

---

## Author

**Ritoma Nandi**  

---
