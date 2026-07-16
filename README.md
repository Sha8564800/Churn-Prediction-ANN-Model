# Customer Churn Prediction using Artificial Neural Network (ANN)

# Project Overview

This project implements an Artificial Neural Network (ANN) using TensorFlow/Keras to predict whether a bank customer is likely to leave (churn) or stay with the bank.

The project covers the complete machine learning workflow including:

- Data preprocessing
- Feature encoding
- Feature scaling
- ANN model building
- Model training
- Model evaluation
- TensorBoard visualization
- Model deployment preparation

# Dataset

Dataset used:
Churn_Modelling.csv

The dataset contains customer information such as:

- Credit Score
- Geography
- Gender
- Age
- Tenure
- Balance
- Number of Products
- Has Credit Card
- Is Active Member
- Estimated Salary

Target Variable:

-> Exited
  - 1 → Customer left the bank
  - 0 → Customer stayed


# Technologies Used

- Python
- TensorFlow / Keras
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- TensorBoard
- Pickle

# Project Workflow

#1. Data Preprocessing

- Removed unnecessary columns
- Label Encoding
- One-Hot Encoding
- Train-Test Split
- Standard Scaling


#2.Model Architecture

```
Input Layer (12 Features)
        │
Dense Layer (64 neurons, ReLU)
        │
Dense Layer (32 neurons, ReLU)
        │
Output Layer (1 neuron, Sigmoid)
```

#3. Compilation

- Optimizer: Adam
- Loss Function: Binary Crossentropy
- Metric: Accuracy


#4. Training

- TensorBoard Callback
- Early Stopping
- Validation Set
- 100 Epochs (with early stopping)


#Results

The model achieved approximately:

- Training Accuracy: ~80%
- Validation Accuracy: ~81–82%

Performance may vary depending on random initialization.


#Installation

Clone the repository

```bash
git clone https://github.com/your-username/customer-churn-ann.git
```

Move into the project directory

```bash
cd customer-churn-ann
```

Create a virtual environment

```bash
python -m venv venv
```

Activate it

### Windows

```bash
venv\Scripts\activate
```

### macOS/Linux

```bash
source venv/bin/activate
```


##Run the Project

Launch Jupyter Notebook

```bash
jupyter notebook
```

Open

```
Project1.ipynb
```


Run all cells sequentially.
# TensorBoard

Start TensorBoard

```bash
tensorboard --logdir logs
```

Open

```
http://localhost:6006
```

to visualize:

- Training Loss
- Validation Loss
- Accuracy
- Histograms

#Saved Files

The project saves:

- `model.h5` → Trained ANN Model
- `scaler.pkl` → StandardScaler
- `ohe_geography.pkl` → One-Hot Encoder
- `label_encoder_gender.pkl` → Label Encoder

These files are used for prediction on new customer data.

---

#Future Improvements

- Hyperparameter tuning
- Dropout layers
- Batch Normalization
- Cross-validation
- Docker containerization

---

## Author

**Utkarsh Jaiswal**

B.Tech Information Technology  
Rajiv Gandhi Institute of Petroleum Technology (RGIPT)

---

## If you found this project useful

Please consider giving it a ⭐ on GitHub.
