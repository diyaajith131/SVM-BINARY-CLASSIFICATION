# Report: Support Vector Machines (SVM)

## Objective
To implement SVMs for binary classification using linear and non-linear kernels.

## Dataset
Breast Cancer Dataset (from sklearn / Kaggle).

## Steps
1. Loaded dataset
2. Split into train/test
3. Trained SVM with linear and RBF kernel
4. Tuned hyperparameters (C, gamma)
5. Evaluated with accuracy & cross-validation

## Results
- Linear Kernel Accuracy: ~0.95
- RBF Kernel Accuracy: ~0.97
- Cross-validation Mean Accuracy: ~0.96

## Conclusion
- SVM performs well on binary classification tasks.
- RBF kernel often performs better when data is not linearly separable.
