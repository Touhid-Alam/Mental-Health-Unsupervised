# Social Media Usage and Mental Health Clustering Analysis

This repository contains the analysis and findings for the research paper: **"Uncovering Latent Patterns in Social Media Usage and Mental Health: A Clustering-Based Approach Using Unsupervised Machine Learning."** This project uses unsupervised machine learning to segment social media users into distinct groups based on their usage patterns and self-reported mental health, revealing nuanced risk profiles that go beyond simple correlations.

## 📌 About The Project

Social media is an integral part of modern life, but its impact on mental health is complex and varies significantly across different individuals. Traditional research often provides broad correlations, overlooking the specific behavioral and demographic patterns that define user experiences.

This study addresses this gap by applying **K-Means clustering** to a dataset of 551 participants. By analyzing demographics, usage habits, and mental health indicators (anxiety, depression, loneliness, sleep quality), we identified six distinct user profiles. Our findings reveal that factors like age, gender, usage intensity, and break-taking habits interact in complex ways, leading to different mental health outcomes. This data-driven segmentation provides a foundation for developing more targeted and effective digital wellness strategies.

### ✨ Key Contributions

*   **Data-Driven Segmentation:** Successfully segmented 551 users into **six distinct clusters** using K-Means, revealing hidden patterns in social media behavior and mental health.
*   **Nuanced Insights:** Moved beyond simple correlations (e.g., "more social media is bad") to identify specific high-risk profiles, such as **'Anxious Student Users'** who report high anxiety despite taking frequent breaks.
*   **Actionable Profiles:** Identified and characterized unique user groups like the resilient **'Low-Break Working Males'** and the vulnerable **'High-Use Male Students'**.
*   **Paradoxical Findings:** Uncovered the "paradox of taking breaks," showing that breaks are not a universal remedy and their effectiveness depends on the user's overall usage pattern.
*   **Targeted Recommendations:** Provided a basis for personalized recommendations for users, platform designers, and mental health professionals.

## 📊 Dataset

The data was collected from **551 participants** via a comprehensive online survey. The survey captured three key areas:
1.  **Demographics:** Age, gender, and occupation.
2.  **Social Media Habits:** Daily hours, primary platform, reason for use, and frequency of taking breaks.
3.  **Mental Health Indicators:** Self-reported levels of anxiety, depression, loneliness, and sleep quality on a 5-point Likert scale.

## ⚙️ Methodology

The project followed a structured, multi-phase approach to analyze the data.
<img width="820" height="147" alt="metho png" src="https://github.com/user-attachments/assets/c41262c2-1f9c-4e81-98b0-ad336d1c162b" />

*Fig 1. The four-phase methodology of the study.*

1.  **Data Preprocessing:**
    *   **Missing Values:** Handled using **KNN Imputation (k=5)** to preserve data relationships.
    *   **Categorical Data:** Converted to numerical format using **One-Hot Encoding**.
    *   **Outliers:** Detected with IQR and Z-scores, then capped at the 1st and 99th percentiles to reduce skew.
    *   **Feature Scaling:** Standardized all numerical features using `StandardScaler` to ensure equal contribution to the clustering algorithm.

2.  **Model Development:**
    *   **Algorithm:** **K-Means Clustering** was chosen for its efficiency and interpretability.
    *   **Optimal Clusters (K):** The optimal number of clusters was determined to be **K=6** by combining the **Elbow Method** and the **Silhouette Score Method**, which peaked at 0.32 for six clusters.
<img width="1183" height="484" alt="elbow" src="https://github.com/user-attachments/assets/174c62ca-7686-45c6-82a8-a5f05557819f" />

    *Fig 2. Determining the optimal K value.*

3.  **Visualization & Interpretation:**
    *   **Dimensionality Reduction:** **Principal Component Analysis (PCA)** was used to reduce the 22 features to 2 principal components for 2D visualization.
    *   **Cluster Profiling:** Cluster centroids were analyzed using a heatmap to identify the defining characteristics of each group.

## 📈 Results: The Six User Profiles

The K-Means model successfully segmented participants into six distinct clusters with a **Silhouette Score of 0.32**. Below is a summary of each profile.

| Cluster ID | Profile Name | Dominant Demographic | Social Media Usage & Break Habits | Key Mental Health Indicators |
| :---: | :--- | :--- | :--- | :--- |
| **0** | **Employed Female Moderators** | Older, Employed Females | Moderate hours, mixed reasons. **61% take breaks.** | Moderate anxiety and sleep issues. |
| **1** | **Anxious Student Users** | Younger, Female Students | Moderate hours. **Highest break-taking (77%).** | **Highest anxiety levels** of all clusters. |
| **2** | **Balanced Male Students** | Younger, Male Students | **Lower hours.** 66% take breaks. | **Lowest anxiety levels.** |
| **3** | **Engaged Female Students** | Younger, Female Students | Higher hours, personal use. 70% take breaks. | Moderate-to-high anxiety. |
| **4** | **Low-Break Working Males** | Older, Employed Males | Moderate hours. **Lowest break-taking (21%).** | **Lowest unhappiness & sleep issues.** |
| **5** | **High-Use Male Students** | Younger, Male Students | Higher hours, personal use. 68% take breaks. | Moderate-to-high anxiety, **highest sleep disturbance.** |

### Visualizations

<img width="1516" height="710" alt="correlation" src="https://github.com/user-attachments/assets/6bd71b38-d39b-4acb-b6d7-490e670a3ab3" />
<img width="868" height="556" alt="pca" src="https://github.com/user-attachments/assets/2b2d7cf6-67ea-4f22-963e-95baa19cfbd4" />


## 💡 Discussion & Key Insights

*   **Demographics Matter:** The impact of social media is not one-size-fits-all. Younger, student-dominated clusters generally reported higher distress than older, employed clusters. Gender-specific patterns also emerged, with female students showing higher anxiety.
*   **Youth and High Usage is a High-Risk Combination:** The clusters with the highest usage among students (Clusters 3 & 5) also reported elevated anxiety and sleep disturbances, confirming that this demographic is particularly vulnerable.
*   **The Paradox of Taking Breaks:** The most intriguing finding is that taking breaks is not a universal solution. The 'Anxious Student Users' (Cluster 1) took the most breaks but had the highest anxiety, suggesting they may be taking breaks *because* they feel distressed, or their breaks are ineffective. In contrast, for 'Balanced Male Students' (Cluster 2), breaks combined with lower usage led to the best outcomes.

## ✅ Recommendations

Based on our findings, we propose the following targeted recommendations:

1.  **For Users:** Cultivate self-awareness to identify your user profile. Practice intentional, purpose-driven social media use and re-evaluate what a "restorative break" means for you (ideally, an offline activity).
2.  **For Platforms & Policymakers:** Design for well-being, not just engagement. Implement features like mindful break reminders and tools to reduce social comparison. Provide researchers with privacy-preserving data access to foster independent studies.
3.  **For Educators & Clinicians:** Integrate digital literacy into curricula, using user profiles as relatable teaching tools. Mental health professionals can use these insights to offer personalized advice beyond generic "reduce screen time" recommendations.

## 🏁 Conclusion

This study successfully demonstrates the power of unsupervised machine learning to uncover nuanced patterns in complex human behavior. By moving beyond broad generalizations, we identified six distinct user profiles, highlighting that the relationship between social media and mental health is highly dependent on a combination of demographic and behavioral factors.

While limited by its cross-sectional, self-reported nature, this research provides a strong foundation for creating personalized, effective digital wellness interventions tailored to the specific needs of different user groups.

## ✍️ How to Cite

If you use this work in your research, please cite the original paper:

```bibtex
@inproceedings{alam2024uncovering,
  title={Uncovering Latent Patterns in Social Media Usage and Mental Health: A Clustering-Based Approach Using Unsupervised Machine Learning},
  author={Alam, Touhid and Shahria, Md All and Mithila, Sanjeda Dewan and Mahmood, Mohammad Sakib and Khatun, Mahfuza},
  booktitle={To Be Published},
  year={2024}
}
