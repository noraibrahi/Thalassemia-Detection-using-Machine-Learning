
# Detecting Beta Thalassemia Disease using Machine Learning and Deep Learning
# Overview
This project presents a hybrid model combining convolutional neural networks (CNN) and a support vector classifier (SVC) to automatically detect beta thalassemia, a rare inherited blood disorder, using both medical imaging and tabular data.

# Motivation
Thalassemia is a challenging disease to diagnose due to its rarity and the potential for misdiagnosis. This project aims to develop an automatic detection system that can aid healthcare professionals in diagnosing thalassemia accurately and efficiently, potentially saving lives by reducing the time and effort required for diagnosis.

# Methodology
## data
### Dataset: The dataset used in this project was provided by Harvard and includes:
Cardiac MRI Scans: 1345 images from 50 patients (37 with thalassemia and 13 controls).
Tabular Data: 50 samples with various attributes including heart and liver parameters.
### Models
- Convolutional Neural Networks (CNN)
- Two separate CNN models were developed for heart and liver MRI images.
- VGG16 and EfficientNet architectures were also tested.
-Support Vector Classifier (SVC)
- Applied to the tabular data with a polynomial kernel.
 Ensemble Model
 - Combines the predictions from CNN models and SVC to achieve higher accuracy.
### Training and Evaluation
- The data was split into training (70%) and testing (30%) sets.
- K-fold cross-validation was applied to ensure robust model evaluation.
### Results
- CNN Model (Heart): 86.45% training accuracy, 84.65% testing accuracy.
- CNN Model (Liver): 92.67% training accuracy, 91.37% testing accuracy.
- Ensemble Model:Achieved a combined accuracy of 91.5% with a 70-30 train-test split and up to 97.2% using K-fold cross-validation.
### Conclusion
The hybrid approach combining CNN and SVC models has proven effective in detecting beta thalassemia. The models developed in this project demonstrate high accuracy and could significantly aid healthcare professionals in diagnosing the disease more efficiently.
## Usage
### Prepare the data by converting DICOM files to PNG:
python dicom2png.py
### Train the models:
python train_models.py
### Evaluate the models:
python evaluate_models.py
