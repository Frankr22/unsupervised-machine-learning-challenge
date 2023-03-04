# Predicting Myopia with Unsupervised Learning
This project is part of a medical research company's effort to find better ways to predict myopia, or nearsightedness, using unsupervised learning techniques. The goal is to identify distinct groups of patients based on their myopia risk factors, which can lead to better predictions of myopia and potentially improve classification models.

## Table of Contents
- Technologies Used
- Data Preparation
- Dimensionality Reduction with PCA
- Clustering with K-Means
- Visualization with t-SNE
- Conclusion and Recommendations

## Technologies Used
- Python 3.8
- Jupyter Notebook
- Scikit-learn
- Pandas
- Matplotlib

## Data Preparation
The data used in this project is stored in a CSV file named myopia.csv. We first read the file into a Pandas DataFrame and remove the "MYOPIC" column, which is the target column for supervised machine learning. We then standardize the data so that columns with larger values do not influence the outcome more than columns with smaller values.

## Dimensionality Reduction with PCA
We use principal component analysis (PCA) to perform dimensionality reduction on the standardized data while preserving 90% of the explained variance. This reduces the number of features from 14 to 10, which capture most of the important information in the data.

## Clustering with K-Means
We use the K-means clustering algorithm to group the patients based on their myopia risk factors. We create an elbow plot to determine the best number of clusters, which appears to be 3 or 4 clusters. We ultimately choose 3 clusters to group the patients.

## Visualization with t-SNE
We use t-distributed stochastic neighbor embedding (t-SNE) to reduce the dimensionality of the PCA-transformed data to two dimensions, which allows us to visualize the clusters. We plot the results using a scatter plot and color each point according to its assigned cluster.

##Conclusion and Recommendations
Based on our unsupervised learning analysis, we recommend using K-means clustering with 3 clusters to group the patients based on their myopia risk factors. This approach could potentially lead to better predictions of myopia by identifying distinct subgroups of patients with similar risk factors. Additionally, clustering the patients separately may be more effective than training on the whole dataset, as our team previously attempted and failed to do.

Overall, this project demonstrates the use of unsupervised learning techniques to gain insights into complex medical data and improve classification models.
