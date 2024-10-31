
# Heart Disease Prediction Project

## Project Description

The Heart Disease Prediction project aims to develop a machine learning model that can predict the likelihood of heart disease based on patient health data and risk factors. The main goal is to assist healthcare professionals in early diagnosis and intervention, thus improving patient outcomes. The project involves data preprocessing, feature engineering, and training classification models to predict the presence or absence of heart disease. Additionally, an interactive user interface is built using Streamlit to make the model accessible for real-world use.

## Table of Contents

- [Installation](#installation)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Preprocessing](#data-preprocessing)
- [Model Training and Fine-Tuning](#model-training-and-fine-tuning)
- [Deployment](#deployment)
- [Usage](#usage)
- [Future Improvements](#future-improvements)
- [License](#license)

## Installation

To run this project locally, you will need the following dependencies:

- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- joblib
- streamlit

You can install the dependencies by running:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib streamlit
```

## Dataset

The dataset used for this project is publicly available on Kaggle. It contains information about various patient health parameters that can be used to predict the presence or absence of heart disease. The dataset includes features such as age, gender, cholesterol level, blood pressure, etc.

**Link to Dataset:** [Heart Disease Data on Kaggle](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data)

## Project Structure

The project is structured as follows:

```
.
├── Heart_Disease_Prediction.ipynb    # Jupyter Notebook containing the analysis and model training
├── heart_disease_app.py              # Streamlit application script
├── heart_disease_rf_model.pkl        # Trained Random Forest model
├── README.md                         # Project README file
```

## Exploratory Data Analysis (EDA)

The project starts by exploring the dataset to understand its structure and identify any patterns or correlations. We analyze the distribution of features, handle missing values, and visualize the correlation between different features using heatmaps. EDA helps in understanding the key factors influencing heart disease.

**Key steps in EDA include:**
- Checking for missing values.
- Summary statistics of the dataset.
- Visualizing correlations between features to determine their relationships.

## Data Preprocessing

Before training the machine learning models, data preprocessing is performed to prepare the dataset for modeling. This includes:

- **Handling Missing Values**: Removing or imputing missing values to ensure the dataset is complete.
- **Encoding Categorical Variables**: Converting categorical features into numeric form using one-hot encoding.
- **Scaling Features**: Standardizing the data using `StandardScaler` to ensure all features contribute equally to the model's training.
- **Splitting the Data**: Dividing the data into training and testing sets using an 80-20 split.

## Model Training and Fine-Tuning

Two machine learning models were trained to predict the likelihood of heart disease:

1. **Logistic Regression**
2. **Random Forest Classifier**

Both models were fine-tuned using `GridSearchCV` to identify the optimal hyperparameters.

- **Logistic Regression**: Tuned using different regularization strengths (`C`) to maximize accuracy.
- **Random Forest**: Tuned for hyperparameters such as the number of estimators, maximum depth, minimum samples split, and minimum samples leaf.

After training, the models were evaluated on the testing set, and the Random Forest model performed slightly better than Logistic Regression, so it was selected for deployment.

## Deployment

The best-performing model (Random Forest Classifier) was saved using `joblib` and deployed using a web application built with Streamlit. The app allows users to input patient health information and receive a prediction about the likelihood of heart disease.

The Streamlit app file is `heart_disease_app.py`. To run the app, use the following command:

```bash
streamlit run heart_disease_app.py
```

## Usage

1. **Clone the Repository**:
   ```bash
   git clone <your-repository-url>
   cd pfsinterns
   ```
2. **Install the Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Streamlit Application**:
   ```bash
   streamlit run heart_disease_app.py
   ```
4. **Provide User Inputs**: The application will prompt you to enter patient details like age, cholesterol levels, chest pain type, etc.
5. **Get Prediction**: Click on the "Predict Heart Disease" button to see if the patient is likely to have heart disease.

## Future Improvements

There are a few areas where the project can be improved:

1. **Feature Engineering**: Adding more health parameters such as ECG data, exercise-induced angina, and other cardiovascular risk factors to improve model accuracy.
2. **Handling Class Imbalance**: Implementing methods like SMOTE to balance the number of instances for each target class and improve model generalization.
3. **Model Interpretability**: Integrating tools like SHAP or LIME to make the model's predictions more interpretable to healthcare professionals.
4. **Advanced Models**: Exploring other models like Gradient Boosting, XGBoost, or an ensemble approach to improve the prediction performance.
5. **User Interface Enhancement**: Improving the Streamlit interface to make it more informative and user-friendly for healthcare practitioners.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to contribute to this project or provide any feedback. Contributions are always welcome!
