## Overview
This project is a beginner-friendly exploration of SAT scores in NYC schools. The objective is to analyze SAT performance trends by borough and identify key insights using Python.

The project is designed to:
- Showcase problem-solving skills in data analysis.
- Provide clear, step-by-step explanations for each stage of analysis.
- Serve as a reference for beginners learning Python, Pandas, and Matplotlib/Seaborn.

Through this project, we examine how borough-level statistics, such as standard deviation and mean SAT scores, can provide insights into school performance.

## Objectives
1. **Analyze borough-level performance:**  
   Identify the borough with the highest variation in SAT scores using standard deviation.

2. **Visualize top-performing schools:**  
   Create visualizations to highlight the schools with the highest combined SAT scores.

## Workflow
The analysis was broken into three main steps:

### Question 1: Create a `total_SAT` Column
We combined the individual scores (Math, Reading, Writing) into a single `total_SAT` column for easier analysis.

### Question 2: Visualize the Top 10 Schools
A bar chart was created to display the top 10 schools based on their combined SAT scores.

### Question 3: Borough Analysis
We calculated borough-level statistics, such as mean and standard deviation, to identify boroughs with the most variation in SAT performance.

The findings and visualizations were saved for reference.

borough_stats = schools.groupby('borough')['total_SAT'].agg(
    std_SAT='std',       
    average_SAT='mean',  
    num_schools='count'  
).reset_index()
largest_std_dev = borough_stats[borough_stats['std_SAT'] == borough_stats['std_SAT'].max()]


---

### **7. Results**
```markdown
## Results
### Key Insights:
1. **Top 10 Schools:**
   The top 10 schools based on combined SAT scores are visualized below:

   ![Top 10 Schools](https://raw.githubusercontent.com/your-username/SCHOOL_SAT_Analysis/main/images/top_10_schools.png)

2. **Borough-Level Analysis:**
   Manhattan has the highest standard deviation in SAT scores, indicating the greatest variability among schools. Here are the borough statistics:

   | Borough    | Num Schools | Average SAT | Std Dev |
   |------------|-------------|-------------|---------|
   | Manhattan  | 89          | 1340.13     | 230.29  |

This variability can help policymakers target borough-specific interventions to reduce disparities.



## Results
### Key Insights:
- Manhattan has the highest standard deviation in SAT scores among boroughs.
- The top 10 schools based on combined SAT scores are visualized below:

![Top 10 Schools](images/top_10_SAT_schools.png)
