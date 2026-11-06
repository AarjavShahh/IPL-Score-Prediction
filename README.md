# IPL-Score-Prediction

## 📌 Project Overview

The **IPL Score Predictor** is a Machine Learning-based web application that predicts the final score of an ongoing Indian Premier League (IPL) cricket match.

The application uses historical IPL match data and a trained Machine Learning regression model to estimate the final innings score based on the current match situation.

Users can enter match details such as batting team, bowling team, current runs, wickets fallen, overs completed, and performance in the last five overs to get a predicted final score range.

## 🎯 Project Objectives

- Predict the probable final score of an ongoing IPL match.
- Analyze historical IPL match data.
- Apply Machine Learning regression algorithms.
- Build an interactive web application using Streamlit.
- Understand the relationship between match conditions and final scores.

## 🛠️ Technologies & Libraries Used

- **Programming Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Web Framework:** Streamlit
- **Model Serialization:** Pickle
- **Development Environment:** Jupyter Notebook, VS Code

## 📂 Project Structure

```text
IPL-Score-Predictor/
│
├── gui.py                   # Streamlit web application
├── iplscoreprediction.ipynb # Data analysis and model training
├── ipl_data.csv             # Historical IPL dataset
├── ml_model.pkl             # Trained Random Forest model
├── requirements.txt         # Project dependencies
└── README.md                # Project documentation
```

## 📊 Dataset Description

The project uses historical IPL match data containing approximately 76,014 records and 15 columns.

Important features include:

| Feature | Description |
|---|---|
| bat_team | Batting team |
| bowl_team | Bowling team |
| runs | Current runs scored |
| wickets | Wickets fallen |
| overs | Overs completed |
| runs_last_5 | Runs scored in the last five overs |
| wickets_last_5 | Wickets taken in the last five overs |
| total | Final innings score (target variable) |

The dataset is processed by:
- Removing irrelevant columns.
- Selecting eight consistent IPL teams.
- Filtering match situations with at least five overs completed.
- Encoding batting and bowling teams using One-Hot Encoding.
- Separating independent and dependent variables.

## 🤖 Machine Learning Models

The following regression algorithms were explored:

1. Decision Tree Regressor
2. Linear Regression
3. Random Forest Regressor
4. Support Vector Regression (SVR)

**Selected Model:** Random Forest Regressor

The Random Forest model was trained using the processed dataset to predict the final IPL innings score.

Model performance was evaluated using:

- R² Score
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)

The trained Random Forest model was exported using Pickle and saved as `ml_model.pkl`.

## ⚙️ Features of the Application

- Interactive Streamlit user interface.
- Selection of batting and bowling teams.
- Input for current match runs and overs.
- Selection of wickets fallen.
- Input for runs and wickets in the last five overs.
- Machine Learning-based final score prediction.
- Displays an estimated score range of ±5 runs around the model prediction.

## 🚀 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/IPL-Score-Predictor.git
```

### 2. Navigate to the Project Directory

```bash
cd IPL-Score-Predictor
```

### 3. Create a Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate the environment:

**Windows:**
```bash
venv\Scripts\activate
```

**Linux / macOS:**
```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the Streamlit Application

```bash
streamlit run gui.py
```

### 6. Open the Application

After executing the command, Streamlit will provide a local URL:

```text
http://localhost:8501
```

Open this URL in your browser to use the IPL Score Predictor.

## 🖥️ How to Use

1. Launch the Streamlit application.
2. Select the batting team.
3. Select the bowling team.
4. Enter the current over and runs scored.
5. Select the number of wickets fallen.
6. Enter runs scored and wickets taken in the last five overs.
7. Click the **Predict Score** button.
8. View the predicted final match score range.

**Note:** The application considers match situations starting from at least five overs to improve prediction reliability. The batting and bowling teams must be different.

## 🔮 Future Improvements

- Integrate real-time IPL match data.
- Improve prediction accuracy through hyperparameter tuning.
- Explore advanced ensemble learning algorithms such as XGBoost.
- Add match-wise prediction analytics and visualizations.
- Deploy the application on Streamlit Community Cloud.
- Update the model using more recent IPL datasets.

## 👨‍💻 Author

**Aarjav Shah**

- GitHub: [Add Your GitHub Profile]
- LinkedIn: [Add Your LinkedIn Profile]

---

⭐ If you find this project interesting, consider giving it a star on GitHub!

**Disclaimer:** This project is developed for educational and machine learning demonstration purposes. Predictions are estimates and do not guarantee actual match results.
