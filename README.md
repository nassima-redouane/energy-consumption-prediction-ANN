# 🔥 Building Energy Consumption Prediction (ANN)

## 📌 Project Overview

This project aims to predict the **heating load (energy consumption)** of buildings using an **Artificial Neural Network (ANN)**.

The dataset used is **ENB2012**, which contains physical characteristics of buildings such as surface area, wall area, glazing, and orientation.

---

## 📊 Dataset

* **768 observations**
* **8 input features**
* **Target variable**: Heating Load (kWh/m²)

---

## ⚙️ Workflow

### 1. Data Exploration

* No missing values
* Bimodal distribution of the target variable
* High variability in energy consumption

### 2. Preprocessing

* Train/Test split (80/20)
* Feature scaling using StandardScaler

### 3. Model Architecture

* Input layer (8 features)
* Hidden Layer 1: 64 neurons (ReLU)
* Hidden Layer 2: 32 neurons (ReLU)
* Output layer: 1 neuron (Linear)

---

## 📈 Model Performance

### Initial Model:

* MAE: 1.73 kWh/m²
* R²: 0.944

### Optimized Model (Random Search):

* MAE: **0.36 kWh/m²**
* R²: **0.997**

---

## 🔍 Hyperparameter Optimization

Random Search was used to test:

* Neurons: (32,16), (64,32), (128,64)
* Learning rate: 0.0005 → 0.01
* Epochs: 50 → 150
* Batch size: 16 → 64

Best configuration:

* **(64,32), lr=0.01, epochs=150, batch_size=16**

---

## 📊 Visualizations

### Distribution of Heating Load

![Distribution](images/distribution_heating_load.png)

### Learning Curve

![Learning Curve](images/courbe_apprentissage.png)

### Model Comparison

![Comparison](images/comparatif_avant_apres.png)

---

## 🧠 Key Insights

* ANN handles non-linear patterns better than linear regression
* Hyperparameter tuning significantly improves performance
* The dataset shows two distinct building energy profiles

---

## 🛠️ Technologies Used

* Python
* TensorFlow / Keras
* Scikit-learn
* Pandas / NumPy
* Matplotlib

---

## 📂 Data Source
The dataset used in this project is publicly available:
Energy Efficiency Dataset (ENB2012)

---

## 📌 Author

Nassima Redouane
