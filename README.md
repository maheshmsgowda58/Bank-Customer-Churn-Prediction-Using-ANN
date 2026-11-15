
# Bank Customer Churn Prediction Using ANN

## 📌 Project Description

The Bank Customer Churn Prediction project is a Deep Learning-based application designed to predict whether a bank customer is likely to leave the bank or continue using its services.

The project uses an Artificial Neural Network (ANN) trained on customer information such as credit score, age, gender, geography, account balance, tenure, number of products, credit card ownership, active membership, and estimated salary.

The dataset is preprocessed using various machine learning techniques, including Label Encoding, One-Hot Encoding, and Feature Scaling. The ANN model learns patterns from historical customer data and predicts the probability of customer churn.

A Streamlit web application is also developed to allow users to enter customer details and receive real-time churn predictions.

## 🎯 Project Objectives

- Analyze bank customer information.
- Preprocess and prepare customer data.
- Apply categorical encoding techniques.
- Standardize numerical features.
- Build and train an Artificial Neural Network.
- Predict customer churn probability.
- Develop an interactive Streamlit application.

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- Pandas
- NumPy
- Scikit-learn
- Streamlit
- Matplotlib

## 📂 Project Structure

```text
Bank-Customer-Churn-Prediction/
│
├── Churn_Modelling.csv
├── app.py
├── experiments.ipynb
├── predictions.ipynb
├── model.h5
├── scaler.pkl
├── label_encoder_gender.pkl
├── onehot_encoder_geo.pkl
├── requirements.txt
└── README.md
```

## 📊 Dataset Information

**Dataset Name:** Churn Modelling

**Input File:** `Churn_Modelling.csv`

**Dataset Size:** 10,000 customer records

The dataset contains the following features:

| Feature | Description |
|---|---|
| CreditScore | Customer credit score |
| Geography | Customer geographical location |
| Gender | Customer gender |
| Age | Customer age |
| Tenure | Number of years with the bank |
| Balance | Customer account balance |
| NumOfProducts | Number of bank products |
| HasCrCard | Credit card ownership |
| IsActiveMember | Active membership status |
| EstimatedSalary | Customer estimated salary |
| Exited | Customer churn status (target) |

## ⚙️ Project Workflow

### 1. Data Collection

Load the customer churn dataset using Pandas.

### 2. Data Preprocessing

The following preprocessing techniques are applied:

- Remove unnecessary columns such as RowNumber, CustomerId, and Surname.
- Encode Gender using Label Encoding.
- Encode Geography using One-Hot Encoding.
- Separate independent and dependent variables.
- Split the dataset into training and testing sets.
- Standardize numerical features using StandardScaler.

### 3. Artificial Neural Network Development

Build an ANN model using TensorFlow and Keras.

**Model Architecture:**

- Input Layer: Accepts customer features.
- Hidden Layer 1: 64 neurons with ReLU activation.
- Hidden Layer 2: 32 neurons with ReLU activation.
- Output Layer: 1 neuron with Sigmoid activation.

**Model Configuration:**

- Optimizer: Adam
- Loss Function: Binary Crossentropy
- Evaluation Metric: Accuracy
- Training Epochs: Up to 100
- Early Stopping: Used during training.

### 4. Model Training

Train the neural network using the training dataset and validate its performance using the test dataset.

### 5. Model Saving

Save the trained model and preprocessing objects:

- `model.h5`
- `scaler.pkl`
- `label_encoder_gender.pkl`
- `onehot_encoder_geo.pkl`

### 6. Customer Churn Prediction

Use the trained ANN model to predict customer churn probability based on the customer's input information.

### 7. Streamlit Web Application

Develop an interactive web application where users can enter customer details, including:

- Geography
- Gender
- Age
- Balance
- Credit Score
- Estimated Salary
- Tenure
- Number of Products
- Credit Card Status
- Active Membership Status

The application displays whether the customer is likely to churn or not, along with the predicted probability.

## 🧠 Model Architecture

```text
       Customer Input Features
                 |
                 v
          Input Layer
                 |
                 v
       Hidden Layer (64)
          ReLU Activation
                 |
                 v
       Hidden Layer (32)
          ReLU Activation
                 |
                 v
        Output Layer (1)
        Sigmoid Activation
                 |
                 v
       Churn Probability
                 |
          -------------
          |           |
          v           v
       Churn       Not Churn
```

## 📦 Installation

Clone the repository:

```bash
git clone <your-repository-url>
```

Navigate to the project directory:

```bash
cd Bank-Customer-Churn-Prediction
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## ▶️ How to Run

Run the Streamlit application:

```bash
streamlit run app.py
```

The application will open in your browser.

Enter the customer information to generate a churn prediction.

## 📈 Prediction Output

The application provides two possible outcomes:

**1. Customer Will Churn**

The model predicts that the customer is likely to leave the bank.

**2. Customer Will Not Churn**

The model predicts that the customer is likely to continue using the bank's services.

The prediction is accompanied by a probability score.

## 💡 Key Learnings

- Understanding Artificial Neural Networks.
- Building deep learning models using TensorFlow and Keras.
- Data preprocessing and feature engineering.
- Label Encoding and One-Hot Encoding.
- Feature Scaling using StandardScaler.
- Training and evaluating neural networks.
- Model saving and loading using H5 and Pickle.
- Developing interactive applications using Streamlit.
- Applying deep learning to real-world business problems.

## 🚀 Future Improvements

- Improve model performance through hyperparameter tuning.
- Add model evaluation metrics such as Precision, Recall, F1-score, and ROC-AUC.
- Add customer churn visualization dashboards.
- Integrate a database to store customer information.
- Deploy the application to a cloud platform.
- Explore additional machine learning algorithms for comparison.

## 📝 Conclusion

The Bank Customer Churn Prediction project demonstrates the application of Artificial Neural Networks in solving a real-world business problem.

By analyzing historical customer information, the model predicts the likelihood of customer churn and provides an interactive interface for generating predictions.

This project provides practical experience in deep learning, data preprocessing, model development, and deployment using Python, TensorFlow, Keras, and Streamlit.

---

**Project Name:** Bank Customer Churn Prediction Using ANN

**Domain:** Machine Learning & Deep Learning

**Programming Language:** Python

**Framework:** TensorFlow / Keras

**Application:** Streamlit
