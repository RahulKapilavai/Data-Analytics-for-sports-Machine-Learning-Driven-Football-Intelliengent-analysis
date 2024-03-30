Football Team Performance Analysis
This repository contains code for analyzing the performance of football teams using various machine learning techniques. The analysis is based on a dataset that includes a wide range of statistics such as defense, receiving, kicking, rushing, and more.

Dataset
The dataset used in this analysis is stored in the football_statss.xlsx file, which contains multiple sheets, each holding different sets of football statistics. The sheets included are:

Defence
kick-off statistics
kick-off return
RECEIVING
Kicking
Punting
Punt_Return
Scoring
Rushing
Analysis Steps
Loading Excel Sheets into Pandas DataFrames: The code starts by importing the necessary libraries, including pandas for data manipulation and analysis. It then loads each sheet from the Excel file into a separate pandas DataFrame within a dictionary, facilitating easy access and manipulation of specific categories of football statistics.
Aggregating DataFrames by Team: The code iterates through each DataFrame and aggregates the data by the 'Team' column, computing the mean of all numeric statistics for each team. This step ensures that each team's statistics are averaged across all entries.
Data Aggregation and Merging Process: The aggregated data from multiple sheets is then merged into a single comprehensive DataFrame, merged_df. This process involves initializing the merged DataFrame with data from the first sheet and iteratively merging each remaining DataFrame based on the 'Team' column.
Preparing Data for Clustering: The dataset is prepared for clustering analysis by separating categorical data, imputing missing values with the mean of the corresponding feature, and standardizing the data to ensure equal contribution of each feature.
Performing K-Means Clustering: The K-Means clustering algorithm is applied to the prepared dataset, grouping teams into three clusters based on their performance metrics. Each team is assigned a cluster label, which is added back to the original DataFrame.
Analyzing Cluster Centers: The centroids of the clusters, representing the mean feature values for each cluster, are converted into a DataFrame for easier interpretation and analysis of the characteristics that define each cluster.
Visualizing Cluster Differences: The code includes functionality for visualizing the differences between clusters based on key performance metrics using bar charts.
ANOVA Test for Feature Comparison: An ANOVA test is performed to identify features that differ significantly across the clusters, providing insights into the key differentiators among the groups.
Imputing Missing Values and Training a Regression Model: Missing values in the dataset are imputed, and a Random Forest Regression model is trained to predict performance based on the team statistics. The model's predictions are added to the original DataFrame, and teams are ranked based on their predicted performance.
Getting Started
To run the code and replicate the analysis, follow these steps:

Install the required Python packages: pip install pandas numpy scikit-learn scipy matplotlib
Place the football_statss.xlsx file in the repository directory.
Run the Jupyter Notebook or Python script containing the analysis code.
Contributing
Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

Acknowledgments
The football statistics dataset used in this analysis was obtained from (https://sports-statistics.com/sports-data/college-football-stats-datasets-csv-database/)
The analysis code utilizes the following Python libraries: pandas, numpy, scikit-learn, scipy, and matplotlib.
