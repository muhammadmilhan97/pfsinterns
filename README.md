# House Price Prediction

This repository contains a project developed as part of the **Pinnacle Full-Stack Interns Data Science Internship**. The goal of this project is to build a machine learning model that predicts house prices based on various features such as location, size, and amenities.

## Project Overview

The project involves the following steps:
1. **Data Preprocessing**: Handling missing data, encoding categorical variables, and scaling numerical features.
2. **Feature Engineering**: Transforming the data into a usable format for machine learning models.
3. **Model Building**: Training a **Linear Regression model** as a baseline to predict house prices.
4. **Model Evaluation**: Evaluating the model's performance using metrics like **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)**.

## Model Performance
- **Mean Absolute Error (MAE)**: 25,610.63
- **Root Mean Squared Error (RMSE)**: 51,965.61

These metrics show the average error in the predictions. The MAE indicates that, on average, the model's predictions are off by around $25,610. The RMSE reflects the overall model error, with larger deviations penalized more heavily.

## Technologies Used
- **Python**
- **Pandas** and **NumPy** for data manipulation
- **Scikit-learn** for machine learning
- **Matplotlib** and **Seaborn** for data visualization

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/muhammadmilhan97/pfsinterns.git
2. Navigate to the directory:
   ```bash
   cd pfsinterns
jupyter notebook House_Price_Prediction_PFSInterns.ipynb

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.
