# Customer Segmentation Using Python
![image](https://github.com/MarkPhamm/Python-Segment-Shopping-Customers/assets/99457952/dbb73f27-a345-4c37-974c-2104d0ce1985)

## Introduction

Customer segmentation is the process of dividing customers into groups based on common characteristics such as demographics, interests, and behavior. The goal is to identify key customer segments to allow for more targeted marketing and product development.

This project performs customer segmentation on mall customer data to identify the key shopping groups based on income, age, and mall shopping score.

## Business Problem

The marketing team wants to identify the most important customer segments to better target marketing activities. The boss has requested an ideal number of segments labeled with a name for each one.

## Technology Used
- **Language**: Python

- **Libraries**:
  - Pandas
  - Seaborn
  - Matplotlib.pyplot
  - Mumpy
  - Sklearn.cluster KMeans
  
## Approach

The following approach was taken:

- **Exploratory Data Analysis**
  - Loaded the data and checked for null values
  - Plotted histograms of the features to understand distributions
  - Calculated summary statistics on the data

- **Preprocessing**
  - Scaled the features for use in K-Means clustering
  - Determined the optimal number of clusters using the elbow method

- **Modeling**
  - Applied K-Means clustering to segment customers
  - Calculated summary statistics on the clusters
  - Named and visualized the clusters

- **Evaluation**
  - Compared cluster assignments to original data
  - Validated clustering performance
  - Assessed cluster distinctiveness

![image](https://github.com/MarkPhamm/Python-Segment-Shopping-Customers/assets/99457952/1328661f-b6f5-4f13-aa48-f479fbc9aee9)

## Key Insights

- 5 clusters provided the ideal segmentation based on the elbow plot
- The clusters showed clear separation based on income, age, and shopping score
- Cluster names were assigned based on distinguishing characteristics
- Visualizations provided additional validation of cluster uniqueness

## Conclusion

This analysis successfully identified 3 key customer segments for the mall using K-Means clustering. These groups can be targeted with tailored marketing strategies based on a deeper understanding of their demographics and shopping behavior. The project demonstrated how unsupervised learning can be leveraged for customer segmentation.

## Future Work

- Incorporate additional features like purchase history
- Apply hierarchical clustering methods
- Implement new customer data to identify updated segments
