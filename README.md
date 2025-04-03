# Integrating Explainable AI Techniques for Anomaly Detection in Encrypted Traffic

## 🎓 Course Project  
This project was developed as part of the **Course Project** at **Vellore Institute of Technology** guided by [Aswani Kumar Cherukuri](https://github.com/cherukuri5). The aim was to integrate **Machine Learning** and **Explainable AI (SHAP)** techniques to detect anomalies in encrypted network traffic. 

## Introduction

In today's interconnected world, network security has become a critical concern. With the rise of encrypted network traffic, traditional monitoring and detection techniques often fall short in identifying potential threats. Encrypted traffic conceals the content of data packets, making it challenging to detect malicious activity. This project focuses on leveraging Explainable AI (XAI) techniques for anomaly detection in encrypted network traffic. By applying machine learning algorithms and using SHAP (SHapley Additive exPlanations) to interpret the models, we can uncover patterns that lead to accurate anomaly detection. The goal is to enhance cybersecurity by providing transparent, interpretable insights into how predictions are made.

Explainable AI is especially vital in network security, as it provides visibility into decision-making processes. Security analysts can trust the predictions of the model, validate results, and take appropriate actions to mitigate threats. This project utilizes three robust machine learning models: XGBoost, Random Forest, and Gradient Boosting. Through SHAP, we interpret the output of these models to understand the key factors contributing to anomalies, enabling faster and more effective decision-making.

---

## Machine Learning Algorithms Used

### 1. XGBoost (Extreme Gradient Boosting)
XGBoost is a powerful gradient boosting algorithm known for its efficiency and accuracy. It employs parallel processing, tree pruning, and regularization techniques to minimize overfitting. Its robust performance makes it ideal for large datasets, and it is often the preferred choice for competitive machine learning challenges. In this project, XGBoost is applied to detect anomalies in encrypted traffic, providing reliable predictions. 

**Accuracy:** **90%**

### 2. Random Forest
Random Forest is an ensemble learning technique that builds multiple decision trees and aggregates their results for improved accuracy. Each tree is trained on a random subset of the dataset using bagging, reducing variance and preventing overfitting. In network anomaly detection, Random Forest is effective due to its resilience to noisy data and its ability to handle complex patterns.

**Accuracy:** **91.5%**

### 3. Gradient Boosting
Gradient Boosting is another powerful ensemble method that builds models sequentially, with each tree minimizing the errors of the previous ones. Unlike Random Forest, which trains trees independently, Gradient Boosting corrects mistakes over iterations, making it a more accurate yet computationally intensive technique. It is well-suited for identifying subtle anomalies in encrypted traffic data. 

**Accuracy:** **90.5%**

### 4. Support Vector Machine (SVM)
Support Vector Machine (SVM) is a supervised learning algorithm that finds an optimal hyperplane to separate different classes. It is particularly effective in high-dimensional spaces and works well for both linear and non-linear classification problems. In anomaly detection, SVM helps distinguish normal traffic from potential threats by maximizing the margin between classes.

**Accuracy:** **99.4%**

### 5. Logistic Regression
Logistic Regression is a simple yet effective statistical model used for binary classification problems. It applies the logistic function to model the probability of an event occurring. While not as complex as ensemble models, logistic regression serves as a strong baseline for anomaly detection in network traffic.

**Accuracy:** **98.4%**

### 6. Perceptron
The Perceptron is a fundamental neural network model that serves as a building block for more advanced deep learning architectures. It learns a linear decision boundary by adjusting its weights based on misclassified examples. Though limited in handling complex, non-linear relationships, it provides insights into basic pattern recognition in network traffic.

**Accuracy:** **92%**

---

## Explainable AI and SHAP

### Explainable AI (XAI)
Explainable AI (XAI) refers to techniques and methods that enable users to understand and interpret machine learning models. In anomaly detection, XAI is essential to ensure transparency and trust in the model's decisions. By interpreting why a particular prediction was made, cybersecurity experts can validate the model's reasoning, identify biases, and improve the overall system.

Using XAI in encrypted traffic anomaly detection has several advantages:
- **Transparency:** Provides insights into model predictions, improving confidence in anomaly detection.
- **Accountability:** Facilitates auditing and compliance with regulatory requirements.
- **Debugging and Improvement:** Helps data scientists identify model weaknesses.
- **Operational Efficiency:** Enables network analysts to focus on the most critical anomalies.

### SHAP (SHapley Additive exPlanations)
SHAP is a widely used XAI technique that interprets model predictions by assigning each feature a Shapley value, representing its contribution to the prediction. Based on cooperative game theory, SHAP values explain the impact of each input feature on the model’s output.

#### **How SHAP Works:**
- **Feature Importance:** SHAP calculates the contribution of each feature to a model’s prediction.
- **Global and Local Interpretability:** It provides both a global understanding of model behavior and local explanations for individual predictions.
- **Visualization:** SHAP summary plots, force plots, and dependence plots offer intuitive insights into feature relationships and their effects on predictions.

#### **SHAP in Anomaly Detection for Encrypted Traffic:**
- SHAP explains why specific network packets were classified as anomalies.
- Analysts can observe feature importance to identify suspicious behavior.
- Provides clarity in understanding complex ensemble models like XGBoost, Random Forest, and Gradient Boosting.
- Allows for effective threat response by identifying the root causes of anomalies.

In this project, SHAP has been applied to generate explanations for the predictions of each model. By visualizing SHAP values, we can clearly interpret the factors contributing to abnormal behavior in encrypted network traffic.


---

## Installation

To set up the project locally, follow these steps:

```bash
# Clone the repository
git clone https://github.com/InflixOP/Anomaly-detection-using-Explainable-AI.git
cd Explainable-AI-Anomaly-Detection

# Create a virtual environment
python -m venv env
source env/bin/activate  # On Windows use 'env\Scripts\activate'

# Install dependencies
pip install -r requirements.txt
```

---

## Dependencies

Ensure you have the following libraries installed:
- Python 3.8+
- pandas
- numpy
- xgboost
- scikit-learn
- shap
- matplotlib
- seaborn

You can install all dependencies using the command:

```bash
pip install -r requirements.txt
```

---

## Usage

1. **Train the Model**: Run the respective script for each model to train it on your dataset.
2. **Evaluate the Model**: Evaluate the performance using accuracy, precision, recall, and F1-score.
3. **Explain the Predictions**: Use SHAP to generate explainable visualizations of model predictions.

Example:
```bash
python train_xgboost.py
python train_random_forest.py
python train_gradient_boosting.py
```

---

## Conclusion

By integrating Explainable AI techniques into anomaly detection for encrypted traffic, this project enhances the transparency and effectiveness of cybersecurity measures. With SHAP's interpretability, security analysts gain a deeper understanding of why certain traffic patterns are classified as anomalous. This enables faster incident response, improved threat mitigation, and a stronger defense against cyber attacks.


