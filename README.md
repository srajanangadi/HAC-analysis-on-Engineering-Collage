# Engineering College Segmentation using Hierarchical Agglomerative Clustering

## Project Overview
This project applies **Hierarchical Agglomerative Clustering (HAC)** to group engineering colleges based on multiple performance parameters. The analysis is useful for identifying college segments and creating targeted recommendations for training programs, placement partnerships, marketing strategies, and student enrollment decisions.

The dataset contains survey-based ratings for 26 engineering colleges, where each college is scored on a standardized scale from **1 to 5** across five criteria:

- Teaching
- Fees
- Placements
- Internship
- Infrastructure

## Objective
The main objective of this project is to segment colleges into meaningful clusters and interpret each cluster as a performance tier.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- SciPy
- Scikit-learn
- Jupyter Notebook

## Methodology
The project follows these steps:

1. Imported required Python libraries.
2. Loaded and explored the engineering college dataset.
3. Checked dataset shape, data types, missing values, and summary statistics.
4. Removed the serial number column before clustering.
5. Created a dendrogram using SciPy’s hierarchical clustering method.
6. Applied **average linkage** for clustering.
7. Cut the dendrogram into 3 clusters using `fcluster`.
8. Created cluster profiles by calculating average scores for each group.
9. Applied `AgglomerativeClustering` from scikit-learn as an additional clustering approach.
10. Generated recommendations based on the final cluster profiles.

## Cluster Summary

| Cluster | Interpretation | Number of Colleges |
|---|---|---:|
| Cluster 1 | Tier 1 / Top-performing colleges | 16 |
| Cluster 2 | Tier 3 / Poor-performing or newer colleges | 2 |
| Cluster 3 | Tier 2 / Medium-performing colleges | 8 |

## Key Insights
- Cluster 1 represents the strongest group of colleges with better teaching, placements, internships, and infrastructure.
- Cluster 2 contains colleges with low teaching, fees, placements, and internship scores, but high infrastructure scores.
- Cluster 3 represents medium-performing colleges that may need support in placements, internships, and infrastructure development.
- Tier 2 and Tier 3 colleges are more suitable targets for training programs because they have greater improvement potential.

## Recommendations
1. Companies looking for placement partnerships should prioritize Tier 1 colleges, followed by Tier 2 colleges.
2. Training providers should target Tier 2 and Tier 3 colleges, as these colleges may benefit more from skill-development programs.
3. Tier 3 colleges should focus on marketing, campus awareness, student engagement, and improving academic outcomes.
4. Students can prioritize Tier 1 colleges while also considering Tier 2 colleges based on their needs and preferences.
