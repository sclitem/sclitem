Datasheet for COVID-19 Chest X-ray Classification Dataset

Motivation

	•	Purpose:

The dataset used for this project is Version 5 of the COVID-19 Radiography Database, which consists of chest X-ray images classified into four categories: COVID-19 positive, normal, lung opacity, and viral pneumonia. A more recent version of the dataset is available, but Version 5 was selected for this project. Additionally, the folders containing lung masks was deleted as it was not used for the task of classifying the chest X-rays.

	•	Creators and Affiliations:
The dataset was developed by a team of researchers from Qatar University, Doha, University of Dhaka, and collaborators from Pakistan and Malaysia, in collaboration with medical doctors. The dataset was created to facilitate research in COVID-19 detection through chest X-ray images.

	•	Funding:
The dataset was likely funded by the participating universities and institutions, with support from research initiatives aimed at combatting the COVID-19 pandemic.


Composition

	•	Instances:
The dataset comprises chest X-ray images, each classified into one of four categories: COVID-19 positive, normal lung images, lung opacity (non-COVID lung infections), and viral pneumonia.

	•	COVID-19 Positive Cases: 3,616 images
	•	Normal Cases: 10,192 images
	•	Lung Opacity Cases: 6,012 images
	•	Viral Pneumonia Cases: 1,345 images
	•	Missing Data:
There is no information indicating missing data. However, some classes (such as viral pneumonia) have significantly fewer instances than others, leading to class imbalances.

	•	Confidentiality:
The dataset does not contain any personally identifiable information (PII) or confidential data such as patient details. It focuses exclusively on chest X-ray images, and legal or medical privacy concerns are not apparent.



Collection Process

	•	Acquisition:
The chest X-ray images were collected from hospitals and healthcare institutions in collaboration with medical doctors. The images were gathered to aid in research during the COVID-19 pandemic, focusing on providing a robust dataset for AI-based diagnosis.

	•	Sampling Strategy:
The dataset was released in stages. The first release contained 219 COVID-19 images, 1341 normal images, and 1345 viral pneumonia images. In subsequent updates, the COVID-19 class was expanded to 3616 images, and additional normal and lung opacity images were added.

	•	Time Frame:
The dataset was collected from the beginning of the COVID-19 pandemic (2020) and continues to be updated as new cases arise.



Preprocessing/Cleaning/Labeling

	•	Preprocessing:
The dataset consists of pre-labeled images, which were classified into their respective categories by medical experts. Some preprocessing (e.g., resizing, normalization) may have been applied to ensure uniformity for machine learning models. Additionally, lung masks were provided in some cases to assist in image segmentation tasks.
	•	Raw Data:
The preprocessed images are made available for machine learning use. It is unclear if the original raw data has been preserved, though lung masks are provided alongside the chest X-ray images for some samples.



Uses

	•	Potential Uses:
The dataset can be used for several tasks, such as:
	•	Training machine learning models for medical image classification.
	•	Detecting and diagnosing COVID-19 and other lung diseases using AI.
	•	Image segmentation tasks using the provided lung masks.
	•	Exploring image enhancement techniques for better X-ray image analysis.
	•	Impact on Future Uses:
The class imbalance, particularly in the viral pneumonia category, could impact the model’s performance, requiring the use of techniques like data augmentation or oversampling to address the imbalance. A dataset consumer should be aware of this limitation to avoid potential performance issues.
	•	Inappropriate Uses:
The dataset should not be used for diagnostic purposes in real-world healthcare settings without proper validation and regulatory approval. It is intended for research and development in AI, and any use that claims definitive diagnosis without further testing could be harmful.



Distribution

	•	Distribution:
The dataset is publicly available on Kaggle: COVID-19 Radiography Database.
	•	License:
The data files are subject to copyright under the original creators. The exact terms can be found on Kaggle’s terms of use for the dataset, and users must adhere to licensing restrictions when using, modifying, or redistributing the data.

Maintenance

	•	Maintenance:
The dataset is updated on a monthly basis by the research group from Qatar University, University of Dhaka, and their collaborators. The team continues to maintain the dataset by adding new X-ray images as they become available.