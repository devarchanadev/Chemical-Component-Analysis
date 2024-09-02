# 🧪 Chemical Component Analysis of Wine Quality

[![Jump to Project Overview](https://img.shields.io/badge/Project%20Overview-📋-blue?style=for-the-badge&logo=read-the-docs)](#project-overview) 
[![Jump to Data Processing](https://img.shields.io/badge/Data%20Processing-📊-blue?style=for-the-badge&logo=analytics)](#data-processing) 
[![Jump to Exploratory Data Analysis EDA](https://img.shields.io/badge/Analysis%20and%20Comparison-🔍-blue?style=for-the-badge&logo=search)](#exploratory-data-analysis-EDA) 
[![Jump to Business Impact](https://img.shields.io/badge/Business%20Impact-💼-blue?style=for-the-badge&logo=business)](#-business-impact) 
[![Jump to Results Visualization](https://img.shields.io/badge/Tools%20and%20Technologies-🔧-blue?style=for-the-badge&logo=tools)](#-results-visualization) 
[![Jump to Business Questions Addressed](https://img.shields.io/badge/Insights%20and%20Recommendations-📝-blue?style=for-the-badge&logo=write)](#-business-questions-addressed) 
[![Jump to Conclusion](https://img.shields.io/badge/Key%20Takeaways-🏆-blue?style=for-the-badge&logo=trophy)](#-conclusion) 


---

[![GitHub Repo](https://img.shields.io/badge/Visit-GitHub_Repo-181717?style=for-the-badge&logo=github)](https://github.com/devarchanadev/Chemical-Component-Analysis) 
[![Dataset Source](https://img.shields.io/badge/Download-Dataset_Source-20BEFF?style=for-the-badge&logo=database)](https://archive.ics.uci.edu/dataset/186/wine+quality)

**Explore the Chemical Properties of Wine 🍷**  
Discover how Principal Component Analysis (PCA), K-Means Clustering, Hierarchical Clustering, and Self-Organizing Maps (SOM) can be leveraged to understand the intricate patterns in wine quality data.

---

## Project Overview

In this project, I analyzed the wine quality data sourced from [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/186/wine+quality) using a blend of machine learning and statistical techniques. My main focus was on uncovering the underlying structure and patterns within the dataset through various methods such as **PCA**, **K-Means Clustering**, **Hierarchical Clustering**, and **Self-Organizing Maps (SOM)**.

The dataset consists of measurements related to various chemical properties of red and white wines. Through both univariate and multivariate analyses, I explored these properties to gain insights into wine quality. Below is a summary of the tools, techniques, and processes used:

| 🔧 **Tools Used**          | 📊 **Techniques Applied**      | 🔍 **EDA Conducted**             |
|----------------------------|--------------------------------|----------------------------------|
| R, RStudio, ggplot2         | PCA, K-Means, Hierarchical Clustering, SOM | Histograms, Boxplots, Correlation Matrix, Scaling |

## Data Processing

The dataset, sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/186/wine+quality), includes measurements of chemical properties for both red and white wines. The combined dataset consists of 13 variables, including continuous, ordinal, and categorical variables.

| 📁 **Data Source** | [Wine Quality Data - UCI Repository](https://archive.ics.uci.edu/dataset/186/wine+quality) |
|-------------------|-----------------------------------------------------------------------------------------|

**Data Cleaning Steps:**
- Merged red and white wine datasets.
- Added a categorical variable "colour" to differentiate between red and white wines.
- Checked for missing values (none were found).
- Scaled the data to prepare for multivariate analysis.

## Exploratory Data Analysis EDA

**Objective:** To understand the distribution, relationships, and potential outliers in the dataset.

**EDA Techniques Applied:**
- **Histograms:** Examined the distribution of each variable, revealing skewness and low variability in some variables.
- **Boxplots:** Identified univariate outliers and potential multivariate outliers using PCA.
- **Correlation Matrix & Heatmap:** Uncovered strong positive and negative correlations between variables, aiding in feature selection for PCA.

<img width="560" alt="Screenshot 2024-09-01 202638" src="https://github.com/user-attachments/assets/967a4723-1310-4321-9717-e79cc21fdd07">
<img width="527" alt="Screenshot 2024-09-01 202703" src="https://github.com/user-attachments/assets/8c4d035b-de9a-4d7c-9046-ca1a9a761663">
<img width="524" alt="Screenshot 2024-09-01 202733" src="https://github.com/user-attachments/assets/77615916-ac97-471f-a988-43df687327b7">
<img width="291" alt="Screenshot 2024-09-01 202806" src="https://github.com/user-attachments/assets/ea2a4959-564f-4270-9a3c-b3b873083481">


### 📈 Example Code Block for EDA:
```r
# PCA for Multivariate EDA
pc_ex <- prcomp(scale(dats), center = TRUE, scale = TRUE)

# Visualize PCA Biplot
fviz_pca_biplot(pc_ex, label = "var", col.ind = wines$colour, shape.ind = km$cluster) +
     labs(title = "PCA Biplot", x = "PC1", y = "PC2")
```
<img width="525" alt="Screenshot 2024-09-01 202832" src="https://github.com/user-attachments/assets/65519e07-6d8f-4c87-8016-b583a5fe1e3e">

## 📊 Business Impact

Understanding the chemical composition of wines is crucial for improving wine quality. By identifying key factors that influence quality, wine producers can make informed decisions about production methods, ultimately leading to better products and increased market value.

### 🔍 Key Insights

- **Cluster Formation:** K-Means clustering identified 2 distinct clusters, while SOM clustering revealed 4 clusters, offering different perspectives on wine classification.
- **Correlations:** Strong positive correlation between `total.sulfur.dioxide` and `free.sulfur.dioxide`, indicating the potential for optimization in sulfur dioxide levels during production.
- **Outliers:** Presence of multivariate outliers that may indicate special cases or anomalies in wine samples.

### 🛠️ Recommendations

- **For Producers:** Focus on optimizing sulfur dioxide levels to enhance wine quality.
- **For Data Scientists:** Always explore both linear (PCA) and non-linear (SOM) methods for clustering to uncover hidden patterns in the data.

## 📈 Results Visualization

- **PCA Biplot:** Shows correlations and variable loadings.
- **K-Means Clustering:** Visualizes clusters formed in the PCA-reduced space.
- **SOM Grid:** Reveals topological relationships between wine samples.
<img width="389" alt="Screenshot 2024-09-01 202922" src="https://github.com/user-attachments/assets/b77c1d35-c40e-4321-adfa-6957a30e8ca8">
<img width="501" alt="Screenshot 2024-09-01 202948" src="https://github.com/user-attachments/assets/0015cea4-6def-4570-bb6d-7af4098fcbaf">
<img width="419" alt="Screenshot 2024-09-01 202859" src="https://github.com/user-attachments/assets/defab97a-6db7-4c91-84b0-db45c4cd0b6e">
<img width="386" alt="Screenshot 2024-09-01 203012" src="https://github.com/user-attachments/assets/639d3095-906a-4ac8-a756-a206ff108149">
<img width="421" alt="Screenshot 2024-09-01 203055" src="https://github.com/user-attachments/assets/b24efc04-7fd5-45a8-a0ca-1fe7a3416353">

## 📝 Business Questions Addressed

- **Quality Differentiation:** How can we classify wines based on their chemical properties?
- **Production Optimization:** Which chemical properties should be controlled to produce higher-quality wines?

### 🧠 Recommendations for Businesses

- Use clustering insights to segment wines and tailor production strategies.
- Consider implementing real-time monitoring systems for chemical properties with high impact on quality.

## 🚀 Conclusion

This project highlights the power of combining PCA, K-Means, and SOM to uncover deep insights from complex datasets. The analysis not only enhances our understanding of wine quality but also offers actionable insights for improving wine production.

### 📊 Statistical Importance

Dimensionality reduction techniques like PCA are essential for simplifying complex datasets, making it easier to visualize and interpret data. Clustering techniques like K-Means and SOM provide different perspectives, each with its strengths.

### 🤔 Why It Matters

As a data scientist, understanding and applying these techniques is crucial for extracting meaningful insights from large, complex datasets. This project serves as a reminder of the importance of thorough EDA and the need to explore data from multiple angles.

### 🏆 Key Takeaways

- **PCA** is invaluable for simplifying and visualizing high-dimensional data.
- **K-Means** offers clear, disjoint clusters, while **SOM** preserves the data's topological structure.
- Always explore data using multiple clustering techniques to uncover hidden patterns.
