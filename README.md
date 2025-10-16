# churn-prediction-streamlit-app


A machine learning project to predict customer churn, built with XGBoost and deployed as an interactive Streamlit web app. This project demonstrates an end-to-end data science workflow, from data analysis and model training to final deployment.

---

## Live Demo

**[➡️ View the Live Churn Prediction App Here!](your-streamlit-app-url-goes-here)**

*(Note: The app may take 30-60 seconds to "wake up" if it has been idle.)*



---

## Project Overview

This project analyzes a dataset of bank customers to predict which individuals are at a high risk of "churning" (closing their accounts). The primary business goal is to identify these at-risk customers so that the bank can proactively offer them incentives to stay, which is more cost-effective than acquiring new customers.

The key challenge in this dataset was a significant **class imbalance**, with far more customers staying than leaving. This required specific techniques to build an effective model that could accurately identify the minority class (churners). After a methodical process of experimentation, a hyperparameter-tuned **XGBoost** model using the `scale_pos_weight` parameter was selected as the champion.

### Key Results
- The final model successfully identifies **82%** of customers who are likely to churn (Recall score of 0.82).
- The most important factors in predicting churn were found to be the **Number of Products**, **Customer Age**, and **Active Member Status**.

---

## Tech Stack
- **Data Analysis & Modeling:** Python, Pandas, Scikit-learn, XGBoost, imblearn
- **Data Visualization:** Matplotlib, Seaborn
- **Web App Deployment:** Streamlit

---

## File Descriptions
- `chrun.ipynb`: A Jupyter Notebook containing the complete, end-to-end process of data exploration, model training, experimentation, and final evaluation.
- `chhrun_pred_2.py`: The Python script for the Streamlit web application.
- `best_churn_model.pkl`: The final, saved champion model.
- `scaler.pkl`: The saved MinMaxScaler used for data preprocessing.
- `requirements.txt`: A list of all Python libraries required to run the project.

---

## How to Run Locally

To run this project on your own machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/sudhanshu768/churn-prediction-streamlit-app.git](https://github.com/sudhanshu768/churn-prediction-streamlit-app.git)
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd churn-prediction-streamlit-app
    ```
3.  **Create and activate a virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```
4.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```
5.  **Run the Streamlit app:**
    ```bash
    streamlit run chhrun_pred_2.py
    ```
