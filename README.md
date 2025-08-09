# Hierarchical Clustering

This project demonstrates the use of **Hierarchical Clustering**, an unsupervised machine learning algorithm, to segment customers based on their spending habits and income levels.  
The dataset used is the **Mall Customers** dataset, containing demographic and spending-related data for mall visitors.

## 📌 Project Overview

The main objectives of this project are:
- To apply hierarchical clustering on customer data.
- To determine the optimal number of clusters using a **dendrogram**.
- To visualize the clustering process for better understanding and business insights.

## 📂 Dataset

**File:** `Mall_Customers.csv`  
**Columns:**
- `CustomerID` – Unique customer identifier.
- `Gender` – Gender of the customer.
- `Age` – Age in years.
- `Annual Income (k$)` – Annual income in thousands of dollars.
- `Spending Score (1-100)` – Score assigned based on customer behavior and spending patterns.

## ⚙️ Requirements

Install the dependencies before running the notebook:

```bash
pip install numpy pandas matplotlib scipy
```

The notebook is designed to run on Google Colab, requiring Google Drive access for the dataset. Ensure the `Mall_Customers.csv` file is stored in your Google Drive at the specified path.

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/hierarchical_clustering.git
   cd hierarchical_clustering
   ```
2. Open the Jupyter Notebook in Google Colab:
   - Upload the `hierarchical_clustering.ipynb` notebook to Google Colab.
   - Ensure the `Mall_Customers.csv` file is available in your Google Drive at the path `/content/drive/MyDrive/Colab Notebooks/Machine Learning A-Z: AI, Python & R + ChatGPT Prize [2024]/Data Sets/Mall_Customers.csv`.
3. Run all cells to:
   - Mount Google Drive.
   - Load the dataset.
   - Generate a dendrogram to find the optimal cluster count.
   - Visualize the clustering process.

## 📊 Methodology

1. **Data Import & Exploration**
   - Load the dataset and inspect its structure.
   - Select `Annual Income (k$)` and `Spending Score (1-100)` for clustering.
2. **Optimal Cluster Selection**
   - Use `scipy.cluster.hierarchy` to create a dendrogram.
   - Identify the optimal number of clusters by analyzing the longest vertical distance without crossing horizontal lines.
3. **Visualization**
   - Use Matplotlib to plot the dendrogram, showing the hierarchical clustering structure.

## 📈 Results

The dendrogram visualizes how customers are grouped based on their income and spending patterns. The results help identify distinct customer segments, such as:
- High income & high spending
- High income & low spending
- Low income & high spending
- Low income & low spending
- Average income & spending

These insights can be used for:
- Targeted marketing strategies.
- Personalized customer experiences.
- Optimizing business decisions.

## 🖼 Sample Output

**Dendrogram for Hierarchical Clustering**  
<img width="707" height="542" alt="image" src="https://github.com/user-attachments/assets/03bc21bf-5f67-4e4f-94aa-ab61d8ca0b9b" />

**Customer Segments Visualization**  
<img width="706" height="547" alt="image" src="https://github.com/user-attachments/assets/9b54f839-192c-4855-9e95-f20ed11e6a62" />
