# Kernel SVM

## Description

- The goal of SVM is to find a decision boundary that best separates the data into different classes.

![kernel_svm](../../images/03_classification/kernel_svm.png)

- In the above image, for the first case, we can draw a line that separates the data into two classes. This is called a `linearly separable data`. For the second case, we cannot draw a line that separates the data into two classes. This is called a `non-linearly separable data`.

- To use SVM for non-linearly separable data, we can use a **`kernel trick`**. This is **a mathematical technique that transforms the data into a higher dimension, where it becomes linearly separable**.

- Once **we have our hyperplane in our 3d space** example and we have our result we can **project it back to the 2d space with our non-linear separator**.

- Mapping to a highr dimension is computationally expensive. So, we use a **kernel function** to map the data to a higher dimension.

### Example: 🤔

![kernel_svm_example1](../../images/03_classification/kernel_svm_example1.png)

- In the above image, we can see that the data is non-linearly separable. We can use a kernel trick to transform the data into a higher dimension, where it becomes linearly separable.

![kernel_svm_example2](../../images/03_classification/kernel_svm_example2.png)

- Now, we can draw a line that separates the data into two classes.

---

## Kernel Functions

- There are many kernel functions. The most common ones are:

  - `Linear Kernel`
  - `Polynomial Kernel`
  - `Radial Basis Function Kernel`, also called the `Gaussian Kernel`
  - `Sigmoid Kernel`

![kernel_svm_rbf](../../images/03_classification/kernel_functions.png)