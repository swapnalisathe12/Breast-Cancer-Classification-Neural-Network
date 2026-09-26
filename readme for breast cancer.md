# Breast Cancer Classification Using Neural Network

## Project Overview

This project implements a Neural Network based classification workflow
for the Scikit-learn Breast Cancer dataset using Python and Google
Colab.

The workflow covers dataset loading, data preparation, train-test
splitting, feature standardization, Neural Network training, model
evaluation, and sample prediction.

## Objective

The objective of this project is to build a classification model that
predicts the tumor class from the available diagnostic features.

## Dataset

-   Total records: **569**
-   Input features: **30**
-   Training records: **455**
-   Testing records: **114**
-   Train-test split: **80:20**

Target classes used in the notebook:

-   `0` → Malignant
-   `1` → Benign

## Technologies Used

-   Python
-   Pandas
-   NumPy
-   Scikit-learn
-   TensorFlow / Keras
-   Matplotlib
-   Google Colab

## Project Workflow

``` text
Dataset
   ↓
DataFrame Creation
   ↓
Feature / Target Separation
   ↓
Train-Test Split
   ↓
StandardScaler
   ↓
Neural Network
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Prediction
```

## Data Preprocessing

The dataset is separated into input features (`X`) and target labels
(`Y`).

The data is divided into training and testing sets using an 80:20 split.

Feature standardization is performed using `StandardScaler`:

``` python
X_train_std = scaler.fit_transform(X_train)
X_test_std = scaler.transform(X_test)
```

The scaler is fitted on the training data and then used to transform the
test data.

## Neural Network Model

The notebook uses the following model structure:

``` text
Input Layer
30 features
     ↓
Hidden Layer
20 neurons
ReLU activation
     ↓
Output Layer
2 classes
Sigmoid activation
```

Training configuration:

-   Optimizer: **Adam**
-   Loss: **Sparse Categorical Crossentropy**
-   Epochs: **10**
-   Validation split: **10%**

## Training Results

At epoch 10, the recorded notebook results were:

  Metric                      Result
  --------------------- ------------
  Training Accuracy       **97.16%**
  Validation Accuracy     **95.65%**
  Training Loss           **0.1176**
  Validation Loss         **0.1163**

## Model Evaluation

The model was evaluated on **114 held-out test records**.

Recorded test accuracy:

**96.49%**

The notebook evaluation output was:

``` text
0.9649122953414917
```

## Sample Prediction

The notebook includes a sample prediction.

Recorded probabilities:

``` text
[0.07750479, 0.9005814]
```

Predicted class:

``` text
1
```

The notebook output describes the sample prediction as:

``` text
The tumor is Benign
```

## Project Files

``` text
Breast-Cancer-Classification/
│
├── README.md
├── Breast_Cancer_Classification_with_Neural_Network.ipynb
├── breast_cancer.csv
├── requirements.txt
├── Breast_Cancer_Classification_Presentation.pptx
│
└── results/
    ├── accuracy_graph.png
    ├── loss_graph.png
    └── prediction_result.png
```

## How to Run

1.  Open `Breast_Cancer_Classification_with_Neural_Network.ipynb` in
    Google Colab.
2.  Upload or provide the required `breast_cancer.csv` file.
3.  Run the notebook cells in order.
4.  Review the training accuracy and loss output.
5.  Run the evaluation cell to obtain test accuracy.
6.  Run the prediction section to view the sample prediction.

## Results Summary

The complete workflow was executed in Google Colab.

-   **97.16%** training accuracy at epoch 10
-   **95.65%** validation accuracy at epoch 10
-   **96.49%** recorded test accuracy
-   **455** training records
-   **114** test records

## Future Scope

Possible extensions include:

-   Hyperparameter tuning
-   Comparing additional classification algorithms
-   Adding a confusion matrix and classification report
-   Creating a simple prediction interface
-   Evaluating the approach on additional datasets

## Note

This is an educational machine-learning project. The model output should
not be treated as a clinical diagnosis.
