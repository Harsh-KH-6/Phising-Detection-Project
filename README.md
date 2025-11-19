# Phishing Detection Project

> A machine learning-based solution for detecting phishing websites, using state-of-the-art models on a large feature-rich dataset. This project includes full data processing, exploration, feature engineering, model training, and evaluation.


## Overview

Phishing is one of the most common cyber threats, with attackers tricking users into revealing sensitive information or installing malware. This project leverages supervised machine learning to classify websites as legitimate or phishing based on a broad set of technical and behavioral features.

The solution preprocesses the data, performs extensive feature engineering, and then trains several models (including XGBoost, Random Forest, and Decision Trees), providing a robust and scalable approach to phishing URL classification.

---

## Features

- **Data Handling**: Loads and explores a large CSV dataset containing real-world URLs and their extracted properties.
- **Preprocessing**: Cleans the data, handles missing values, normalizes numerical features, and converts categorical data.
- **Feature Extraction**: Uses up to 89 features, including URL-based, domain-based, and third-party metrics.
- **Multi-model Training**: Supports XGBoost, Random Forest, Decision Trees, Logistic Regression.
- **Metrics**: Evaluates with confusion matrix, ROC curves, and detailed classification reports.
- **Google Colab Ready**: Includes Colab badge for easy launch.

---

## Dataset and Features

- The data is loaded from a CSV file and processed using Pandas.
- Features include:
  - URL length, hostname length, presence of special characters (e.g., "@" or "-"), count of dots/hyphens, use of HTTPS, proxy/IP presence.
  - Domain registration length, age, WHOIS info, web traffic, Google index, and page rank.
  - Label column (`status`): `legitimate` (0) or `phishing` (1).

**Sample Columns**:
```
['url', 'length_url', 'length_hostname', 'ip', 'nb_dots', 'nb_hyphens', 'nb_at', ..., 'status']
```

---

## Model Training and Evaluation

- Data is split into training and testing sets (e.g., 8001 train, 3429 test).
- All features are scaled for model compatibility.
- Models are trained using Scikit-learn and XGBoost:

  - **Confusion Matrix**: Visualizes performance for each model.
  - **ROC Curve**: Compares true positive and false positive rates.
  - **Classification Report**: Shows precision, recall, and F1-score.

**Metrics Example** (Random Forest, 97% accuracy):
```
              precision    recall  f1-score   support
           0       0.97      0.97      0.97      1760
           1       0.97      0.97      0.97      1669
    accuracy                           0.97      3429
   macro avg       0.97      0.97      0.97      3429
weighted avg       0.97      0.97      0.97      3429
```

**ROC Curve Comparison**:
- All models are plotted for visual comparison.

---

## Installation & Usage

> You can run this project directly in Google Colab!

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Harsh-KH-6/Phising-Detection-Project/blob/main/phising_detection_.ipynb)

### Requirements

- Python 3.x
- pandas, numpy, scikit-learn, xgboost, matplotlib (see notebook for exact package usage)

### Steps

1. Clone this repository or open the notebook in Google Colab.
2. Upload your dataset CSV when prompted.
3. Run all cells for data preprocessing, training, and evaluation.
4. View the results (metrics, confusion matrices, ROC curves).

---

## Results

- XGBoost, Random Forest, and Decision Trees were compared.
- High accuracy, precision, and recall achieved across models.
- Saved metrics and feature importance for reproducibility.

---

## Contributing

Contributions, suggestions, and improvements are always welcome! Open an issue or submit a pull request.

---


## Author

Maintained by [Harsh-KH-6](https://github.com/Harsh-KH-6).
