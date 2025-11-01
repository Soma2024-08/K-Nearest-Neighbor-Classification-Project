# K-Nearest-Neighbor-Classification-Project
A machine learning project that illustrates the use of the K-Nearest Neighbors algorithm from scratch. Here, multiple distance metrics were compared, decision boundaries were visualized, model performance was evaluated using confusion matrices and classification reports, and the best value of k for the highest accuracy was identified
# **Introduction**
The K-Nearest Neighbors (KNN) algorithm is a simple yet powerful supervised machine learning technique used for both classification and regression problems. In this project, we focus on classification. The algorithm works by storing all the available data points and classifying new data points based on a similarity measure—most commonly distance functions. When a new example is introduced, KNN finds the K nearest data points from the training set and assigns the most common label among them as the predicted class.
<p align="center">
  <img src="0_ItVKiyx2F3ZU8zV5.png" width="500"/>
</p>
The figure below illustrate the yellow square represents a new sample that needs to be classified, and the nearby red stars and green triangles represent two different classes. The class of the new point is determined based on the majority of its nearest neighbors.
---
## This implementation provides:
-Support for multiple distance metrics: Euclidean, Manhattan, Minkowski, Cosine, and Hamming.
-Automatic determination of the best K value based on validation accuracy.
-Visualization of accuracy vs K for each distance metric.
-Confusion matrix and classification report for detailed evaluation.
-Decision boundary plots to visualize model predictions in 2D (via PCA).
----
## ✨ Features of the Project

This implementation provides:

- **Support for multiple distance metrics:** Euclidean, Manhattan, Minkowski, Cosine, and Hamming  
- **Automatic determination of the best K value** based on validation accuracy  
- **Visualization of accuracy vs K** for each distance metric  
- **Confusion matrix and classification report** for detailed evaluation  
- **Decision boundary plots** to visualize model predictions in 2D (via PCA)

---

## 📈 Performance Evaluation

The model was evaluated by varying both **K values** and **distance metrics**.  
The following plot shows how validation accuracy changes with different values of K for each metric.

From the plot, it can be observed that the **Euclidean**, **Manhattan**, and **Minkowski** metrics perform the best for smaller K values, while **Cosine** and **Hamming** show relatively lower accuracy.  
This highlights the **sensitivity of KNN** to the choice of distance metric.
Below is the summary of the best K value and accuracy obtained for each distance metric used during experimentation:
<p align="center">
  <img src="output1.png" width="500"/>
</p>

The **Minkowski** and **Manhattan** distance metrics achieved the highest accuracy of **97.37%**,  
demonstrating their effectiveness for this dataset.

---

## 🧾 Confusion Matrix and Model Results

To further analyze the model’s performance, a **confusion matrix** was generated for the best-performing configuration —  
**Minkowski distance with K = 3**.

The confusion matrix below shows the count of correctly and incorrectly classified samples.
<p align="center">
  <img src="output2.png" width="500"/>
</p>
---

## 🧮 Classification Report

The classification report below provides detailed metrics — **precision**, **recall**, and **F1-score** — for each class.  
It reflects how well the model distinguishes between the two classes.
| Label | Precision | Recall | F1-Score | Support |
|:------|:----------:|:-------:|:--------:|--------:|
| **0** | 1.0000 | 0.9028 | 0.9489 | 72 |
| **1** | 0.8571 | 1.0000 | 0.9231 | 42 |
| | | | | |
| **Micro Avg** | 0.9386 | 0.9386 | 0.9386 | 114 |
| **Macro Avg** | 0.9286 | 0.9514 | 0.9360 | 114 |
| **Weighted Avg** | 0.9474 | 0.9386 | 0.9394 | 114 |

These results show that the model achieves **strong performance across both classes**,  
maintaining a good trade-off between precision and recall.

---

##  Decision Boundary Visualization

The decision boundary plot provides an **intuitive understanding** of how KNN separates classes in a 2D projection (using PCA).  
The plot below shows regions predicted for each class when using **Euclidean distance with K = 3**.

The red and green regions correspond to the two predicted classes,  
while the scatter points represent training and testing data.  
The smooth transitions across boundaries demonstrate the **non-parametric nature of KNN**.

<p align="center">
  <img src="output3.png" width="500"/>
</p>
As we can see, the model performs exceptionally well, correctly classifying the majority of samples.  
Only a few misclassifications occurred in one of the classes, indicating a **strong balance between precision and recall**
---

