# CodeAlpha_Credit_Scoring_Model

📌 Credit Scoring Model Explanation
The Credit Scoring Model predicts an individual's creditworthiness based on their transaction history. It classifies individuals into three categories:
1️⃣ Good Credit (0) – Low spending, stable transactions
2️⃣ Average Credit (1) – Moderate spending, occasional high transactions
3️⃣ Bad Credit (2) – High spending, irregular patterns

🔹 How It Works
1️⃣ Data Processing
The dataset consists of credit card transactions with features like:
Amount (transaction value)
Card Type (Gold, Platinum, etc.)
Exp Type (Shopping, Bills, etc.)
Gender
Year, Month of transaction
We clean the data by converting categorical values into numerical values.
Feature Engineering creates new columns like Spending_Category (Low, Medium, High).
2️⃣ Model Training
The target variable Creditworthiness is assigned based on spending behavior.
The model uses Random Forest Classifier, which:
Learns patterns from past transactions.
Determines how spending habits relate to creditworthiness.
The dataset is split into training (80%) and testing (20%) sets.
3️⃣ Model Evaluation
Accuracy is measured using:
Precision, Recall, and F1-score.
Confusion Matrix (how well the model distinguishes Good/Average/Bad credit).
Expected accuracy: 85-90% (varies based on dataset quality).
4️⃣ Real-Time Prediction
The trained model is saved using joblib for deployment.
A Flask or FastAPI API is created to serve predictions.
Users can send new transaction data, and the API will return:
json
Copy
Edit
{"Creditworthiness": "Average"}
🔹 Why This Model?
✅ Helps banks evaluate customer credit risk.
✅ Enables real-time loan approvals based on spending behavior.
✅ Can be improved with more financial history data.
