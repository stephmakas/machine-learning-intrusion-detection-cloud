# Machine-Learning-Based Intrusion Detection for Cloud Environments

## Project Overview

This is an academic/portfolio project exploring the use of machine learning for network intrusion detection in cloud environments.

The project uses network traffic datasets to investigate whether machine-learning models can distinguish normal network activity from malicious traffic. The work was carried out in Python using Jupyter Notebook and includes data preprocessing, model training, evaluation, visualization, and interpretation of results.

## Objectives

The main objectives of the project were to:

* Prepare and clean network traffic data for machine-learning analysis.
* Develop a model for detecting malicious network activity.
* Evaluate model performance using classification metrics and confusion matrices.
* Investigate different attack categories and identify challenges in detecting less frequent attacks.
* Examine the features that contributed most to the final model's predictions.

## Tools and Technologies

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Random Forest
* Logistic Regression
* CSV network traffic datasets

## Dataset and Attack Types

The experiments included network traffic associated with:

* DDoS attacks
* PortScan attacks
* Web attacks
* BENIGN/normal traffic

The data was cleaned and prepared before model training and evaluation.

## Machine Learning Approach

The project involved data preprocessing followed by supervised machine-learning experiments.

The models investigated included:

* Random Forest
* Logistic Regression

For the combined DDoS and PortScan experiment, the traffic was converted into two classes:

* BENIGN
* ATTACK

The models were evaluated using accuracy, precision, recall, F1-score, and confusion matrices.

## Results

### Combined DDoS and PortScan Detection

The final Random Forest model achieved approximately:

* **Accuracy:** 99.994%
* **Precision:** 100%
* **Recall:** 99.990%
* **F1-score:** 99.995%

The confusion matrix showed very few misclassified attack samples in the test set.

### Web Attack Detection

The Web Attack experiment achieved approximately:

* **Overall accuracy:** 98.77%

However, the results also showed an important limitation: the model detected only a small proportion of the attack samples compared with the BENIGN class.

This demonstrates why overall accuracy alone is not sufficient when evaluating intrusion-detection systems, especially when the dataset contains severe class imbalance.

## Feature Importance

Feature-importance analysis was performed on the final Random Forest model to investigate which network traffic characteristics contributed most strongly to the model's predictions.

The repository contains the resulting feature-importance visualization.

## Project Structure

```text
machine-learning-intrusion-detection-cloud/
│
├── intrution_detection.ipynb
│
├── Final_Confusion_Matrix.png
├── Final_Feature_Importance.png
├── Web_Attack_Confusion_Matrix.png
├── DDoS_Model_Accuracy.png
│
└── README.md
```

## What I Learned

Through this project, I gained practical experience with:

* Loading and inspecting real-world network traffic data.
* Data cleaning and preparation.
* Binary and multiclass classification concepts.
* Training and evaluating machine-learning models.
* Interpreting confusion matrices and classification metrics.
* Understanding the effect of class imbalance on intrusion-detection results.
* Using feature importance to interpret a machine-learning model.
* Documenting a technical project and its limitations.

## Project Limitation

One important finding was that a high overall accuracy does not necessarily mean that an intrusion-detection model detects all attack types effectively.

The Web Attack experiment demonstrated this limitation, particularly for less frequent attack classes. Further work could explore class balancing, additional algorithms, feature selection, and more advanced approaches for improving minority-class detection.

## Author

**Stephinie Akpaeva**

This repository represents an academic/portfolio project completed to develop and demonstrate practical skills in Python, machine learning, data analysis, and cybersecurity.

It is presented as a project portfolio piece and does not represent previous professional experience in machine learning or cybersecurity.
