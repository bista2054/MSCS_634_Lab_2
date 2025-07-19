# KNN and RNN Classifiers on Wine Dataset

## Purpose
This lab explores the performance of **K-Nearest Neighbors (KNN)** and **Radius Neighbors (RNN)** classifiers using the Wine Dataset from the sklearn Python library. The goal is to understand how different parameter values (number of neighbors for KNN and radius size for RNN) impact classification accuracy and to visualize and compare the results to guide optimal parameter selection.

## Key Insights
- **KNN Accuracy Trends:** Accuracy generally improved with increasing k up to a certain point (around k=11 or 15), then plateaued or slightly decreased, indicating that a moderate number of neighbors helps balance bias and variance.
- **RNN Accuracy Trends:** Accuracy varied with radius size; smaller radii often missed neighbors leading to lower accuracy, while overly large radii included too many points, sometimes reducing precision.
- **Model Comparison:** In this dataset, KNN achieved slightly higher and more stable accuracy compared to RNN, suggesting fixed neighbor counts are effective when data points are relatively evenly distributed.
- **Practical Implication:** KNN is preferable when a consistent number of neighbors is desired, while RNN can be useful in datasets with varying density where distance thresholds are more meaningful.

## Challenges and Decisions
- Finding the right radius values for the Radius Neighbors classifier was tricky.  
  - Too small a radius meant not enough neighbors were found for some points.  
  - Too large a radius sometimes lowered accuracy by including too many neighbors.  
  - To handle cases with no neighbors, I set the model to assign the most common class.

- Choosing the range of k and radius values involved balancing enough options for insight without making the process too slow.

- I considered scaling features because KNN and RNN use distance, but since the dataset’s features were already on similar scales, I skipped it for this lab. However, feature scaling might be needed in other datasets.


---
