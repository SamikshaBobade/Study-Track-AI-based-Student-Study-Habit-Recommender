# Milestone 2: Clustering and Pattern Detection

## Objectives

### 1. Feature Selection & Preparation for Clustering
- Selected 3–4 numerical features from the student dataset.
- Standardized the selected features using **StandardScaler**.
- Applied **Principal Component Analysis (PCA)** to reduce dimensions for 2D visualization.

### 2. Apply Clustering Algorithm
- Implemented **K-Means Clustering**.
- Chose **k = 3** as the optimal number of clusters.
- Predicted and assigned cluster labels to each student.

### 3. Add Cluster Labels
- Added a new column `Cluster` to the DataFrame.
- Calculated the mean of selected features for each cluster to summarize cluster characteristics.

### 4. Visualize Clustering Results
Visualizations created using **Matplotlib** and **Seaborn**:

- **Scatter Plot (PCA 2D):** Shows clusters in two dimensions using PCA.  
- **Bar Plot:** Displays the mean values of features per cluster.  
- **Box Plot:** Compares the distribution of `final_exam_score` across clusters.  
- **Pie Chart:** Shows the distribution of samples in each cluster.

### 5. Interpretation & Insights
Cluster summaries and insights were displayed in a table format using color gradients for clarity.

**Example Insights:**

| Cluster | Description |
|----------|-------------|
| 0 | High-performing students with strong quiz, assignment, and exam scores. |
| 1 | Moderate performers with balanced study time and average results. |
| 2 | Low-performing or struggling students with lower academic scores. |

---

## Key Learnings
- Feature scaling and PCA help in achieving meaningful clusters.
- K-Means clustering can reveal performance patterns among students.
- Visual analysis supports better interpretation of clustering outcomes.
  

