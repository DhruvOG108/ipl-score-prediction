# 🏏 IPL Score Prediction using Deep Learning

## 📌 Overview

This project focuses on predicting the **total score in an IPL match** using **Deep Learning techniques**. By analyzing historical match data (2008–2017), the model learns patterns between teams, players, venues, and match situations to generate accurate score predictions.

---

## 🚀 Project Highlights

* End-to-end Deep Learning pipeline
* Real IPL dataset analysis
* Neural Network regression model
* Interactive prediction system using widgets

---

## 🛠️ Tech Stack

* Python
* NumPy, Pandas
* Matplotlib, Seaborn
* Scikit-learn
* TensorFlow, Keras
* ipywidgets

---

## 📂 Dataset

The dataset contains IPL match data with features such as:

* Venue
* Batting Team & Bowling Team
* Batsman & Bowler
* Runs, Wickets, Overs
* Match ID & Date

---

# 🔄 Project Workflow (Step-by-Step)

## 1️⃣ Installing Libraries

Imported required libraries for:

* Data handling
* Visualization
* Machine Learning
* Deep Learning

---

## 2️⃣ Loading the Dataset

* Loaded dataset using Pandas
* Previewed initial rows using `.head()`

---

## 3️⃣ Exploratory Data Analysis (EDA)

Performed analysis to understand data patterns:

* Matches played per venue
* Top 10 batsmen by runs
* Top 10 bowlers by wickets
* Visualized using bar plots

---

## 4️⃣ Label Encoding

* Converted categorical features into numeric values
* Used `LabelEncoder`
* Stored encoders for reuse

---

## 5️⃣ Feature Selection

* Dropped irrelevant columns: `date`, `mid`
* Used correlation heatmap
* Removed highly correlated features:

  * `runs_last_5`
  * `wickets_last_5`
  * `non-striker`

---

## 6️⃣ Splitting the Dataset

* Selected input features and target variable
* Split data into training and testing sets:

  * 70% training
  * 30% testing

---

## 7️⃣ Feature Scaling

* Applied **Min-Max Scaling**
* Scaled features between **0 and 1**
* Ensured consistent model performance

---

## 8️⃣ Building the Neural Network

* Used Keras Sequential model

* Architecture:

  * Input layer
  * 2 hidden layers (ReLU activation)
  * Output layer (Linear activation)

* Loss Function: **Huber Loss**

* Optimizer: **Adam**

---

## 9️⃣ Training the Model

* Trained model on scaled data
* Parameters:

  * Epochs: 10
  * Batch Size: 64
* Validated using test data
* Plotted training vs validation loss

---

## 🔟 Evaluating the Model

* Predicted scores on test data
* Used evaluation metric:

  * Mean Absolute Error (MAE)

📊 **MAE ≈ 14.41**

---

## 1️⃣1️⃣ Interactive Score Prediction

* Built using **ipywidgets**

* User can input:

  * Teams
  * Venue
  * Players
  * Match stats (runs, wickets, overs)

* Model predicts score in real-time

---

## 🧠 Model Architecture

```python id="model123"
model = keras.Sequential([
    keras.layers.Input(shape=(9,)),
    keras.layers.Dense(512, activation='relu'),
    keras.layers.Dense(216, activation='relu'),
    keras.layers.Dense(1, activation='linear')
])
```

---

## 📈 Results

* Accurate real-time predictions
* Handles outliers using Huber Loss
* Good generalization on unseen data

---

## 🎯 Example Prediction

* Match: CSK vs RCB
* Venue: Chinnaswamy Stadium
* Predicted Score: **152 runs**

---

## 📌 Key Concepts Used

* Deep Learning (Neural Networks)
* Regression
* Feature Engineering
* Data Visualization
* Model Evaluation

---

## 🔮 Future Improvements

* Use latest IPL datasets
* Try advanced models (LSTM, GRU)
* Hyperparameter tuning
* Deploy using Streamlit or Flask

---

## 🤝 Contributing

Feel free to fork this repository and contribute improvements.

---

## 📜 License

This project is open-source and available under the MIT License.

---

## ⭐ Support

If you found this helpful, please give it a ⭐ on GitHub!
