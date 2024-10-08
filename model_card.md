Model Card: COVID-19 Chest X-ray Classification

Model Description

Input:
The input to the model consists of chest X-ray images, categorized into four classes: COVID-19 positive, normal lung images, lung opacity (non-COVID lung infections), and viral pneumonia.

Output:
The model outputs a prediction of one of the four categories: COVID-19 positive, normal, lung opacity, or viral pneumonia. The prediction is a classification label based on the features extracted from the input X-ray images.

Model Architecture:
The model employs an XGBoost classifier, a gradient boosting decision tree algorithm. Hyperparameter optimization was performed using Optuna to enhance performance. The model classifies the X-ray images into one of the four categories based on learned patterns from the dataset.

Performance

The model was evaluated on the test set using standard classification metrics:

	•	Test Accuracy: 72.34%
	•	Class-wise Performance:
	•	COVID-19: Precision: 0.67, Recall: 0.67, F1-Score: 0.67
	•	Lung Opacity: Precision: 0.67, Recall: 0.61, F1-Score: 0.63
	•	Normal: Precision: 0.79, Recall: 0.81, F1-Score: 0.80
	•	Viral Pneumonia: Precision: 0.63, Recall: 0.75, F1-Score: 0.68

The evaluation was conducted on a 15% test split of the COVID-19 Radiography Database (Version 5).

Limitations

	•	Limited GPU access: Computational constraints limited model complexity and prevented the exploration of deeper architectures, such as ensemble learning or further optimization.
	•	Data constraints: The model’s performance is limited by the data, especially in under-represented classes (e.g., viral pneumonia), where the F1-scores are lower.
	•	Cloud computing: The steep learning curve for cloud computing and restricted access affected the ability to fully test and train more advanced models.

Trade-offs

	•	Model simplicity: The XGBoost model, while efficient, was chosen due to resource limitations. More complex architectures (such as convolutional neural networks or ensemble methods) could potentially perform better but were impractical in the current environment.
	•	Computational efficiency vs. accuracy: The model trades off accuracy for computational efficiency, given the constraints of cloud computing and limited access to high-performance GPU resources.

While there are better models available for this task, the limitations around computing resources, and the need to simplify the approach to suit available infrastructure, led to the selection of this model. Future work could explore more advanced solutions with improved infrastructure.

