
COVID-19 Chest X-ray Classification Project

Non-Technical Explanation of Your Project

This project aims to build a machine learning model to classify chest X-rays into four categories: COVID-19 positive, normal lung images, lung opacity (non-COVID infections), and viral pneumonia. The model uses convolutional neural networks (CNNs) to identify patterns in the images that correspond to each condition, assisting in the early diagnosis of lung diseases, including COVID-19.

Data

The dataset used is Version 5 of the COVID-19 Radiography Database, consisting of X-ray images categorized into four classes:

	•	COVID-19 Positive Cases: 3,616 images
	•	Normal Cases: 10,192 images
	•	Lung Opacity (Non-COVID Lung Infections): 6,012 images
	•	Viral Pneumonia Cases: 1,345 images

Total dataset size: 21,165 X-ray images. The dataset is split into training, validation, and test sets using a 70/15/15 split ratio to ensure a balanced distribution across classes.

Dataset Access:
The dataset can be accessed from https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database.

Citation:
1. M.E.H. Chowdhury et al., “Can AI help in screening Viral and COVID-19 pneumonia?” IEEE Access, Vol. 8, 2020, pp. 132665 - 132676. [Paper link](https://ieeexplore.ieee.org/document/9144185)
2. Rahman, T. et al., “Exploring the Effect of Image Enhancement Techniques on COVID-19 Detection using Chest X-ray Images,” 2020. [Paper link](https://doi.org/10.1109/ACCESS.2020.3011329)

Model

Initially, the project experimented with convolutional neural networks (CNNs) for classification, but after evaluation, I decided to revert to an XGBoost model. XGBoost is highly effective for structured data and performs well in tabular data formats.

XGBoost Model Details:

	•	Optimization: Hyperparameters were optimized using Optuna, a library for automatic hyperparameter optimization. Key hyperparameters tuned were:
	•	max_depth: Maximum depth of a tree.
	•	learning_rate: Step size for gradient descent.
	•	n_estimators: Number of boosting rounds.
	•	min_child_weight: Minimum sum of instance weight.
	•	subsample: Proportion of samples used for training each tree.
	•	colsample_bytree: Proportion of features used for training each tree.
	•	gamma: Regularization parameter to control model complexity.
The Optuna study explored 20 different parameter combinations to maximize validation accuracy. The final parameters were applied to the complete training and validation datasets for the final model.
	•	Objective: Multiclass classification with four output classes: COVID-19, normal, lung opacity, and viral pneumonia.

Results

The XGBoost model was evaluated on the test set, and the following metrics were obtained:

Test Accuracy: 72.34%

Performance by Class:

	•	COVID-19:
	•	Precision: 0.67
	•	Recall: 0.67
	•	F1-Score: 0.67
	•	Support: 723 images
	•	Lung Opacity:
	•	Precision: 0.67
	•	Recall: 0.61
	•	F1-Score: 0.63
	•	Support: 1203 images
	•	Normal:
	•	Precision: 0.79
	•	Recall: 0.81
	•	F1-Score: 0.80
	•	Support: 2038 images
	•	Viral Pneumonia:
	•	Precision: 0.63
	•	Recall: 0.75
	•	F1-Score: 0.68
	•	Support: 269 images

Overall Metrics:

	•	Accuracy: 0.72
	•	Macro Average Precision: 0.69
	•	Macro Average Recall: 0.71
	•	Macro Average F1-Score: 0.70
	•	Weighted Average F1-Score: 0.72

Class Distribution in Final Predictions:

	•	Normal: 2094
	•	Lung Opacity: 1094
	•	COVID-19: 721
	•	Viral Pneumonia: 324

Contact Details:
GitHub repository: https://github.com/sclitem/sclitem





