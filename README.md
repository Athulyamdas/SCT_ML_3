# 🐾 Cat vs Dog Image Classifier using SVM and GridSearchCV

This project is a simple **image classification** system that distinguishes between **cats and dogs** using a **Support Vector Machine (SVM)** classifier with **GridSearchCV** optimization. The model is trained on resized image data and includes dimensionality reduction using **PCA** for better performance and reduced computation.

---

## 📁 Dataset

The dataset is structured like this:

Skillcraft_Technologies/
└── task_3/
├── training_set/
│ ├── cats/
│ └── dogs/
└── test_set/
├── cats/
└── dogs/

Each subdirectory contains `.jpg` images of cats and dogs.

---

## 🚀 Project Workflow

### 🔸 Step 1: Importing Required Libraries

Essential Python libraries like `numpy`, `pandas`, `sklearn`, `matplotlib`, and image processing libraries like `skimage.io` and `skimage.transform` are imported.

### 🔸 Step 2: Image Preprocessing

- Images are loaded using `imread()` and resized to **40x40x3** (RGB).
- Flattened into 1D arrays of 4800 features.
- Labeled `0` for cats and `1` for dogs.
- Final data is stored in a `DataFrame`.

### 🔸 Step 3: Train-Test Split

Dataset is split into 80% training and 20% testing using train_test_split() with stratified sampling.

### 🔸 Step 4:Dimensionality Reduction with PCA

PCA (Principal Component Analysis) is used to reduce feature dimensions from 4800 to 300.

Helps improve training speed and reduce overfitting.

### 🔸 Step 5:Model Building with SVM

🧠 What is SVM?
SVM (Support Vector Machine) is a powerful supervised learning algorithm used for classification. It works by finding the optimal hyperplane that separates data points of different classes with the maximum margin.

⚙️ Kernel Used
This project uses the RBF kernel (Radial Basis Function) which is suitable for non-linear classification problems.

### 🔸 Step 6:Model Optimization with GridSearchCV

🔍 What is GridSearchCV?
GridSearchCV is used to automate hyperparameter tuning. It tests multiple combinations of model parameters using cross-validation to find the best performing model.

### 🔸 Step 7: Model Evaluation

Predictions are made using the best model found by GridSearchCV.

Accuracy and classification report (precision, recall, F1-score) are printed.

### 🔸 Step 8: Single Image Prediction

Any test image is resized to 40x40x3, flattened, transformed using the trained PCA object, and passed to the model for prediction.
