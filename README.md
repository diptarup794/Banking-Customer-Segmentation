# Bank Customer Clustering Using K-Modes Clustering Algorithm

## Overview
This project demonstrates the use of the K-Modes clustering algorithm to segment customers of a Portuguese banking institution based on various categorical attributes. The data used in this demonstration is from the UCI Machine Learning Repository, specifically the Bank Marketing dataset.

## Data Source
The data is related to direct marketing campaigns (phone calls) of a Portuguese banking institution. The dataset can be found [here](https://archive.ics.uci.edu/ml/datasets/bank+marketing).

## Dataset Description
The dataset contains several attributes, but for this demonstration, we focus only on the categorical attributes:
- `age` (numeric, converted to categorical)
- `job`: type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
- `marital`: marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
- `education`: (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
- `default`: has credit in default? (categorical: 'no','yes','unknown')
- `housing`: has housing loan? (categorical: 'no','yes','unknown')
- `loan`: has personal loan? (categorical: 'no','yes','unknown')
- `contact`: contact communication type (categorical: 'cellular','telephone')
- `month`: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
- `day_of_week`: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
- `poutcome`: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')

## Steps to Perform Clustering

### 1. Data Reading and Initial Understanding
First, we load the dataset and explore its structure to understand the attributes and their data types.

### 2. Data Cleaning
We check for any null values in the dataset and find that there are none. Thus, no additional cleaning is needed.

### 3. Data Preparation
The `age` attribute, which is numeric, is converted into categorical bins. This helps in using K-Modes which works with categorical data.

### 4. Label Encoding
We use label encoding to convert categorical variables into numerical values suitable for clustering algorithms.

### 5. Clustering with K-Modes
We use two different initialization methods for K-Modes clustering: "Cao" and "Huang". The K-Modes algorithm is applied to segment the customers into different clusters.

### 6. Choosing the Optimal Number of Clusters
We use the cost function to determine the optimal number of clusters by plotting the cost against the number of clusters and choosing the point where the cost significantly drops.

### 7. Cluster Analysis and Visualization
We analyze the resulting clusters by visualizing the distribution of attributes within each cluster. This helps in understanding the characteristics of each cluster.

## Results and Visualization
The clusters are visualized using count plots for various attributes, segmented by the predicted clusters. This helps in identifying the unique characteristics of each cluster, which can be useful for targeted marketing strategies.

## Conclusion
The K-Modes clustering algorithm effectively segments the customers based on categorical attributes. This segmentation can be used by the bank to tailor their marketing campaigns to different customer segments, potentially increasing the effectiveness of their marketing efforts.


## How to Run
1. Clone the repository.
2. Place the `bankmarketing.csv` file in the `data/` directory.
3. Open the Jupyter notebook `bank_customer_clustering.ipynb` and run the cells to perform clustering and visualize the results.
4. Alternatively, run the `k_modes_clustering.py` script to execute the clustering process.

## Requirements
- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- kmodes



