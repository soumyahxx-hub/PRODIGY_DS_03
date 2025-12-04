🌳 Decision Tree Classifier – Bank Marketing Dataset

This project builds a Decision Tree Classifier to predict whether a bank customer will subscribe to a term deposit based on demographic and behavioral attributes.
It uses the UCI Bank Marketing Dataset, applying preprocessing, model training, evaluation, and visualization of the decision tree and confusion matrix.

📁 Project Structure
Decision_Tree_Classifier/
│
├── train_tree.py              # Training script
├── predict.py                 # Single-sample prediction script
├── tree_pipeline.joblib       # Saved model + preprocessor
├── bank.csv                   # Dataset (if included locally)
├── decision_tree.png          # Decision Tree visualization
├── confusion_matrix.png       # Confusion Matrix visualization
├── README.md                  # Project documentation
├── requirements.txt           # Python dependencies
└── .gitignore                 # Ignored files (venv, logs, large files)

🎯 Objective

The goal of this project is to:

Train a Decision Tree to classify whether a customer will subscribe (yes) or not (no)

Preprocess categorical and numerical data automatically

Save the preprocessing + model as a pipeline

Evaluate the model using accuracy score and confusion matrix

Visualize the decision tree structure and predictions

Allow single predictions via predict.py

🧠 Model Overview
Algorithm Used

DecisionTreeClassifier from scikit-learn

Preprocessing

OneHotEncoding for categorical features

No scaling for numeric features (Decision Trees don’t require scaling)

Output

tree_pipeline.joblib → Contains fitted preprocessor + model

📊 Model Performance (example)
Metric	Score
Accuracy	~0.88
Precision (macro)	~0.70
Recall (macro)	~0.63
F1-score (macro)	~0.65

(scores depend on train/test split)

🖼️ Visualizations
Decision Tree

Confusion Matrix

▶️ How to Run This Project
1. Install dependencies
pip install -r requirements.txt

2. Train the model
python train_tree.py


This will:

Load the dataset

Train the Decision Tree

Save the model as tree_pipeline.joblib

Generate visualizations

🤖 Making Predictions

Use predict.py to run predictions on a single sample.

python predict.py


Example output:

Prediction (1 = yes, 0 = no): 0
Probabilities: [0.982 0.017]


Modify the sample input inside predict.py to test different customers.

📦 Dependencies
pandas
numpy
scikit-learn
matplotlib
joblib


(Automatically installed via requirements.txt)

🏆 Key Skills Demonstrated

Data preprocessing

Decision Tree modeling

Data visualization

Pipeline creation

Model persistence using Joblib

Prediction script development

Version control with Git & GitHub

📄 License

This project is licensed under the MIT License.
Feel free to use, modify, and distribute this project.

🚀 Future Improvements

Hyperparameter tuning with GridSearchCV

Compare with Logistic Regression / Random Forest

Deploy model via Flask/FastAPI

Build Streamlit UI for predictions
