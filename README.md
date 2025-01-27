# Data Science Assignment: eCommerce Transactions Dataset

## Overview
This repository contains the solutions for the eCommerce Data Science assignment, which involves performing exploratory data analysis (EDA), building a lookalike model, and customer segmentation using clustering techniques. The dataset consists of three files: `Customers.csv`, `Products.csv`, and `Transactions.csv`, providing customer details, product information, and transaction data, respectively.

## Dataset Description

The dataset contains the following files:

### 1. **Customers.csv**  
This file contains information about customers who made purchases on the eCommerce platform.
- **CustomerID:** Unique identifier for each customer.
- **CustomerName:** Name of the customer.
- **Region:** Continent where the customer resides (e.g., Asia, Europe, etc.).
- **SignupDate:** The date when the customer signed up on the platform.

### 2. **Products.csv**  
This file provides information about the products sold on the platform.
- **ProductID:** Unique identifier for each product.
- **ProductName:** Name of the product.
- **Category:** Category to which the product belongs (e.g., electronics, fashion, etc.).
- **Price:** Price of the product in USD.

### 3. **Transactions.csv**  
This file contains transactional data for each sale.
- **TransactionID:** Unique identifier for each transaction.
- **CustomerID:** ID of the customer who made the transaction (foreign key linked to `Customers.csv`).
- **ProductID:** ID of the product sold (foreign key linked to `Products.csv`).
- **TransactionDate:** The date when the transaction occurred.
- **Quantity:** Number of units purchased in the transaction.
- **TotalValue:** Total value of the transaction (calculated as `Quantity * Price`).
- **Price:** Price of the product sold in that specific transaction.

## Features of the Code

### 1. **Exploratory Data Analysis (EDA)**
   - **Objective:** Perform EDA on the eCommerce dataset to explore and understand customer behavior, product trends, and transaction patterns.
   - **Operations:**
     - Data cleaning (handling missing values, duplicates).
     - Descriptive statistics (mean, median, mode, etc.).
     - Data visualizations (histograms, bar plots, heatmaps) to understand distributions and correlations.
     - Insights into customer and product performance based on sales and regions.

### 2. **Lookalike Model**
   - **Objective:** Build a recommendation system that finds similar customers based on profile and transactional behavior.
   - **Operations:**
     - Combine customer data and product transaction data.
     - Use similarity metrics (e.g., cosine similarity, Euclidean distance) to compare customer profiles and transaction history.
     - Recommend top 3 most similar customers for each of the first 20 customers.

### 3. **Customer Segmentation / Clustering**
   - **Objective:** Perform customer segmentation using clustering techniques to identify distinct customer groups.
   - **Operations:**
     - Combine customer profile information with transaction data.
     - Use clustering algorithms such as K-Means to segment customers.
     - Evaluate clustering quality using metrics like Davies-Bouldin Index.

## Jupyter Notebook Code Description

The project includes Jupyter Notebooks to perform the tasks outlined:

- **EDA:** The EDA notebook covers the entire process from loading the dataset to cleaning the data and performing in-depth analysis. Key visualizations like histograms, box plots, and scatter plots are used to derive insights from the dataset.
- **Lookalike Model:** The notebook for the Lookalike Model walks through the steps of building a recommendation system using customer and product data. It includes feature engineering, calculating similarity scores, and creating a list of top 3 lookalike customers for the first 20 customers.
- **Customer Segmentation:** The clustering notebook covers the implementation of K-Means clustering, including preprocessing, feature selection, and calculating clustering evaluation metrics like the Davies-Bouldin Index. The clusters are visualized using PCA to understand customer behavior patterns.

## Running the Code
1. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
