# SVM Interview Questions

1. What is a support vector?**

A **support vector** is a data point that lies closest to the decision boundary (hyperplane) in an SVM model. These points are crucial because they:

* **Define the position and orientation** of the hyperplane.
* **Directly affect the margin** (the distance between the hyperplane and the nearest data points).

If you removed a support vector, the hyperplane would likely change.

---

2. What does the C parameter do?**

The **C parameter** controls the **trade-off between achieving a low training error and a large margin**:

* **Small C**: Larger margin, allows more misclassifications → better generalization (less overfitting).
* **Large C**: Focuses on minimizing training error, smaller margin → risk of overfitting.

Think of it as how much you **penalize misclassification**.

---

3. What are kernels in SVM?**

A **kernel** is a function that transforms the input data into a **higher-dimensional space** where it may become linearly separable. SVMs use kernels to handle **non-linear data**.

Common kernels include:

* **Linear**
* **Polynomial**
* **Radial Basis Function (RBF)**
* **Sigmoid**

---

4. What is the difference between linear and RBF kernel?**

| Feature         | Linear Kernel                               | RBF Kernel                                 |
| --------------- | ------------------------------------------- | ------------------------------------------ |
| Mapping         | No mapping needed (works in original space) | Maps data to infinite-dimensional space    |
| Use case        | When data is linearly separable             | When data has complex, non-linear patterns |
| Computation     | Faster and simpler                          | More computationally intensive             |
| Hyperparameters | Only C                                      | C and gamma                                |

---

5. What are the advantages of SVM?**

* **Effective in high-dimensional spaces**
* Works well with clear margin of separation
* Memory efficient (uses only support vectors)
* Can use **different kernel functions** for non-linear decision boundaries
* Robust to overfitting, especially in high-dimensional spaces

---

6. Can SVMs be used for regression?**

Yes. It's called **Support Vector Regression (SVR)**.

* SVR tries to fit the best line within a **threshold (epsilon)**, such that most data points fall within it.
* It uses similar concepts (support vectors, margin, kernel) as classification SVMs.

---

7. What happens when data is not linearly separable?**

SVM can still work in two main ways:

1. **Use soft margin**: Allow some misclassifications using the **C parameter**.
2. **Use kernel trick**: Map the data to a higher-dimensional space where it **becomes linearly separable**.

---

8. How is overfitting handled in SVM?**

Overfitting is handled by:

* **Regularization (C parameter)**: A smaller C allows more slack, reducing overfitting.
* **Choosing the right kernel**: Complex kernels (like high-degree polynomial) can overfit.
* **Tuning gamma (in RBF kernel)**: High gamma means each point has narrow influence → risk of overfitting.

Proper **cross-validation and hyperparameter tuning** are key to avoiding overfitting.

