# Milestone 3: Recommendation Engine

This milestone implements the steps of the AI-based Student Study Habit Recommender: generating actionable recommendations for students using cluster analysis results.

## Overview

After clustering students based on their study-related behaviors and academic performance (from Milestone 2), Milestone 3 delivers targeted recommendations and study plans for each cluster/group. Insights help educators and students improve strategies tailored to their respective profiles.

## Features

- **Cluster Analysis Summaries:** Aggregates and displays mean values for all key features per cluster (`ClusterID`).
- **Specific Recommendations:** Each cluster receives a tailored summary, recommendation list, and weekly study plan.
- **Personalized Guidance:** Individual suggestions and motivation strategies provided for sample students from each cluster.
- **Visualizations:** Distribution of students across clusters for analytical insights.
- **Reusable Recommendation Functions:** Functions to generate and display student-specific advice based on cluster membership and behavior.


## Clusters & Recommendations

- **Cluster 0: High Performers**
  - *Insight:* Consistent and balanced results
  - *Recommendations:* Maintain current habits, seek advanced/challenging projects, consider research involvement
  - *Plan:* Revise thoroughly, take mock tests weekly, pursue advanced self-directed learning

- **Cluster 1: Average Performers**
  - *Insight:* Steady with potential for growth
  - *Recommendations:* Focus on weak topics, join study groups, maintain a consistent revision schedule
  - *Plan:* Study weak subjects daily, complete a practice paper weekly, attend tutorials

- **Cluster 2: Low Performers**
  - *Insight:* Need for structure and support
  - *Recommendations:* Seek mentorship, increase practice frequency, focus first on foundational concepts
  - *Plan:* Study with breaks, attempt daily quizzes, discuss challenges weekly

## Example Output

See notebook tables for per-cluster summaries and detailed, actionable recommendations, such as:

| Aspect           | Details                                                                    |
|------------------|----------------------------------------------------------------------------|
| Cluster Insight  | High performers – consistent and balanced results across assessments.       |
| Recommendations  | - Maintain current study patterns<br>- Explore advanced opportunities      |
| Weekly Plan      | - Revise two subjects weekly<br>- Attempt mock tests<br>- Self-paced learning|

## Visualization

A plot (`matplotlib/seaborn`) displays how students are distributed across clusters for easy inspection.

## Files

- `recommendation_engine.ipynb` : Jupyter notebook containing the code, functions, and outputs
- `final_clustering_dataset.csv` : Input dataset required, must contain `ClusterID` for each student.


