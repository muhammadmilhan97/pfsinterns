
# Credit Card Fraud Detection Using Ensemble Learning

This project demonstrates the development of a fraud detection system for credit card transactions using various ensemble learning techniques. The goal is to accurately identify fraudulent transactions using models such as Random Forest, Gradient Boosting, and XGBoost. The project covers data preprocessing, feature engineering, model training, evaluation, and a simple UI for making predictions.

## Project Overview

The dataset used for this project contains transaction details, including anonymized features and labels indicating whether a transaction is fraudulent (`1`) or legitimate (`0`). Ensemble learning algorithms are employed to achieve high accuracy in identifying fraudulent activities. 

The following steps are involved in this project:
1. **Data Preprocessing** - Cleaning and scaling the data.
2. **Model Training** - Training various ensemble learning models.
3. **Evaluation** - Evaluating the performance of the models using metrics like accuracy, precision, recall, F1-score, and ROC-AUC.
4. **Saving the Best Model** - Saving the best-performing model (XGBoost) for future use in making predictions.

## Technologies Used
- **Python**: Main programming language.
- **Pandas**: Data manipulation and analysis.
- **Scikit-learn**: Machine learning algorithms and evaluation metrics.
- **XGBoost**: Optimized gradient boosting for model training.
- **Matplotlib & Seaborn**: Data visualization tools.
- **Joblib**: Saving and loading the trained models.

## Installation

### Prerequisites
Before running the project, ensure you have the following Python libraries installed:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost
- joblib

You can install these libraries using `pip`:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost joblib
```

### Cloning the Repository
Clone the repository to your local machine using Git:

```bash
git clone https://github.com/muhammadmilhan97/pfsinterns.git
```

### Running the Project
1. Navigate to the project folder:

```bash
cd pfsinterns
```

2. Run the Jupyter notebook (`CreditCardFraud_Detection_PFSInterns.ipynb`) or execute the Python script to train and evaluate the models.

## Steps Involved
1. **Data Exploration**:
   - Loaded and explored the dataset.
   - Checked for missing values and class distribution.

2. **Data Preprocessing**:
   - Scaled the "Time" and "Amount" features using `StandardScaler`.
   - Split the dataset into training and testing sets.

3. **Model Training and Evaluation**:
   - Trained Random Forest, Gradient Boosting, and XGBoost models.
   - Evaluated models based on metrics like accuracy, precision, recall, F1-score, and ROC-AUC.
   - XGBoost achieved the highest performance in detecting fraud.

4. **Model Deployment**:
   - Saved the trained XGBoost model for future use in predictions.

## Results

### Model Performance Metrics:
- **Random Forest Classifier**:
  - Accuracy: 0.9996
  - Precision: 0.9524
  - Recall: 0.8163
  - F1 Score: 0.8791
  - ROC-AUC: 0.9528

- **Gradient Boosting Classifier**:
  - Accuracy: 0.9983
  - Precision: 0.5294
  - Recall: 0.1837
  - F1 Score: 0.2727
  - ROC-AUC: 0.3469

- **XGBoost Classifier**:
  - Accuracy: 0.9995
  - Precision: 0.9186
  - Recall: 0.8061
  - F1 Score: 0.8587
  - ROC-AUC: 0.9743

### Best Model:
The **XGBoost** model achieved the highest performance across multiple metrics, making it the best choice for fraud detection in this case.

## Future Enhancements
- Implementing **imbalanced data handling** techniques (e.g., SMOTE or ADASYN) for better model performance in real-world applications.
- Adding **real-time prediction** capability using a web interface (e.g., Flask, Streamlit).
- Exploring other advanced machine learning models, such as neural networks.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- The dataset was sourced from [Kaggle: Credit Card Fraud Detection](https://www.kaggle.com/datasets).
- Special thanks to the community for providing valuable resources and tutorials on machine learning and fraud detection.
