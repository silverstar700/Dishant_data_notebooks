# Credit Card Fraud Detection Pipeline

Welcome to my personal data science project! This repository contains an end-to-end Python notebook dedicated to identifying fraudulent credit card transactions. 

## 📊 About the Dataset
The dataset used in this project was sourced from **Kaggle**. It is one of the most famous, highly regarded benchmarking datasets for anomaly detection and class imbalance problems in the data science community, containing real-world European cardholder transactions.

### 1. Exploratory Data Analysis (EDA) & Data Insights
* **Class Imbalance Inspection:** Confirmed the imblanace in dataset showing extreme scarcity of fraudelent transactions (<1%), proving that standard evaluation metrics like basic "Accuracy" are entirely misleading.
* **Distribution Analysis:** Analyzed feature spreads to identify highly skewed variables requiring statistical transformation.

### 2. Advanced Data Preprocessing
* **Outlier & Skew Management:** Applied **Log Transformations** to skewed features(Amount) to normalize their distribution.
* **Robust Scaling:** Utilized `RobustScaler` to scale features, ensuring that extreme transaction outliers wouldn't negatively bias the linear model.
* **Stratified Splitting:** Implemented stratified data splitting to guarantee that both the training and testing sets maintained the exact same ratio of fraud-to-normal transactions.

### 3. Model Training & Heavy Optimization
* **Algorithm:** Developed a **Logistic Regression** classification baseline.
* **Class Weight Tuning:** Rather than relying on generic oversampling, I manually tuned and optimized the `class_weight` parameter (testing up to a 1:30 ratio) to force the model to prioritize the rare fraud cases.
* **The ROC-AUC Trap:** Explicitly analyzed why standard ROC-AUC metrics provide an overly optimistic view on imbalanced datasets

---

## 🛠️ How to View and Run
1. Open the `Credit_card_dataset_fraud_detection.ipynb` file directly here on GitHub to view the full pipeline, markdown explanations, and charts.
2. Dataset can be found in the 'Dataset' folder with the name 'creditcard.csv'. Alternatively, you can download the file from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) 
3. To interact with or run the code, click the **"Open in Colab"** badge at the top of the notebook file.` file here on GitHub.
2. Click the **"Open in Colab"** badge at the top of the file.
3. Upload your dataset or update the data-loading path, and run all cells sequentially.
