# Google Play Store App Analysis 📱

This project is a complete data analysis of the Google Play Store dataset from Kaggle. The goal is to identify key factors that influence an app's user rating and its success on the platform.

---

## 🎯 Project Goal

The main question this analysis seeks to answer is: **"What features (like Category, Price, Installs) have the biggest impact on an app's user rating?"**

A machine learning (regression) model was built to predict app ratings based on these features.

---

## 🛠️ Process & Methodology

The project follows the standard data analysis workflow:

1.  **Data Cleaning:**
    * Loaded the `googleplaystore.csv` dataset.
    * Cleaned the `Installs` column (removed `+` and `,` characters).
    * Cleaned the `Price` column (removed `$` symbol).
    * Cleaned the `Size` column (converted `M` to megabytes, `k` to megabytes, and filled `Varies with device` with the mean).
    * Dropped rows with missing `Rating` values.
    * Removed a famous "bad row" where data was shifted.

2.  **Exploratory Data Analysis (EDA):**
    * Analyzed the distribution of `Rating` (most apps are rated highly).
    * <img width="855" height="545" alt="output3" src="https://github.com/user-attachments/assets/62db3769-4596-4b7e-ae44-f64075b74b58" />

    * Visualized the number of apps per `Category`.
    * 
    * Compared the ratings of `Free` vs. `Paid` apps using a boxplot.
<img width="688" height="545" alt="output1" src="https://github.com/user-attachments/assets/bd966f01-46b7-4d1b-b72d-c430e96b3b65" />

3.  **Feature Engineering:**
    * Converted the `Type` column to `0` (Free) and `1` (Paid).
    * Applied One-Hot Encoding to the `Category` and `Content Rating` columns to prepare them for the model.

4.  **Machine Learning Modeling:**
    * Built a **Random Forest Regressor** to predict the `Rating`.
    * Split the data into 80% training and 20% testing sets.
    * Trained the model and evaluated it using **Mean Absolute Error (MAE)**.
    * <img width="792" height="453" alt="image" src="https://github.com/user-attachments/assets/6a7a8d1c-5bad-485b-8947-a1af89a55169" />
    <img width="1045" height="699" alt="output" src="https://github.com/user-attachments/assets/1e3c961f-2d42-4e9a-bbe1-a35f89108aee" />



---

## 📊 Key Findings

(This is where you put your answer from Step 6!)

The analysis of feature importances from the model revealed that the most significant factors for predicting an app's rating are:

* **Feature 1:** (e.g., `Reviews` - Apps with more reviews tend to have...)
* **Feature 2:** (e.g., `Size` - The size of the app had a...)
* **Feature 3:** (e.g., `Installs` - ...)

*(Look at your "Feature Importance" chart and write a few bullet points here)*

---

## 💻 Technologies Used

* **Python**
* **Pandas:** For data loading and cleaning.
* **Matplotlib & Seaborn:** For data visualization.
* **Scikit-learn (sklearn):** For splitting data and building the Random Forest model.
* **Jupyter Notebook:** As the development environment.

---

## 🚀 How to Run

1.  Clone this repository.
2.  Install the required libraries: `pip install pandas matplotlib seaborn scikit-learn`
3.  Run the `YourNotebookName.ipynb` file in Jupyter Notebook.
