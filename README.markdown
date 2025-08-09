# Hierarchical Clustering Analysis

## Overview
This repository contains a Jupyter Notebook (`hierarchical_clustering.ipynb`) that demonstrates the implementation of hierarchical clustering using Python. The notebook analyzes customer data to identify distinct groups based on their annual income and spending score, utilizing hierarchical clustering techniques and a dendrogram to determine the optimal number of clusters.

## Dataset
The notebook uses the `Mall_Customers.csv` dataset, which contains information about mall customers, including:
- **CustomerID**: Unique identifier for each customer.
- **Genre**: Gender of the customer (Male/Female).
- **Age**: Age of the customer.
- **Annual Income (k$)**: Customer's annual income in thousands of dollars.
- **Spending Score (1-100)**: Score assigned to the customer based on their spending behavior.

The analysis focuses on the `Annual Income (k$)` and `Spending Score (1-100)` columns to perform clustering.

## Requirements
To run the notebook, you need the following Python libraries:
- `numpy`
- `pandas`
- `matplotlib`
- `scipy`

You can install these dependencies using pip:
```bash
pip install numpy pandas matplotlib scipy
```

Additionally, the notebook is designed to run on Google Colab, which requires mounting Google Drive to access the dataset. Ensure you have the dataset file (`Mall_Customers.csv`) stored in your Google Drive under the path specified in the notebook.

## Usage
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```
2. **Upload to Google Colab**:
   - Open Google Colab and upload the `hierarchical_clustering.ipynb` notebook.
   - Ensure the `Mall_Customers.csv` file is available in your Google Drive at the path `/content/drive/MyDrive/Colab Notebooks/Machine Learning A-Z: AI, Python & R + ChatGPT Prize [2024]/Data Sets/Mall_Customers.csv`.
3. **Run the Notebook**:
   - Execute the cells in sequence to:
     - Mount Google Drive.
     - Import necessary libraries.
     - Load and preprocess the dataset.
     - Generate a dendrogram to identify the optimal number of clusters.
   - The notebook produces a dendrogram visualization to help determine the number of clusters based on Euclidean distances and the Ward linkage method.

## Notebook Structure
- **Mounting Google Drive**: Connects to Google Drive to access the dataset.
- **Importing Libraries**: Loads `numpy`, `pandas`, and `matplotlib` for data manipulation and visualization, and `scipy` for hierarchical clustering.
- **Loading the Dataset**: Reads the `Mall_Customers.csv` file and displays the first few rows.
- **Data Preprocessing**: Selects the `Annual Income (k$)` and `Spending Score (1-100)` columns for clustering.
- **Dendrogram Visualization**: Uses `scipy.cluster.hierarchy` to create a dendrogram, helping to identify the optimal number of clusters by analyzing Euclidean distances with the Ward linkage method.

## Outputs
- A dendrogram plot displaying the hierarchical clustering structure, with customers on the x-axis and Euclidean distances on the y-axis.
- The dendrogram helps visually determine the optimal number of clusters by identifying the longest vertical distance without crossing horizontal lines.

## Notes
- The notebook assumes the dataset is located in a specific Google Drive path. Update the file path in the notebook if your dataset is stored elsewhere.
- The clustering is performed using the Ward linkage method, which minimizes the variance within clusters. Other linkage methods can be explored by modifying the `method` parameter in the `sch.linkage` function.
- This analysis is part of an unsupervised learning approach to segment customers for targeted marketing or business strategies.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.