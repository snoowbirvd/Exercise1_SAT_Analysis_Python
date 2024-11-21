## Overview
Given: [school.csv](data/school.csv)

### Question 1: Which NYC schools have the best math results?
The goal of this question is to identify schools with the best math results, defined as schools that scored at least 80% of the maximum possible math score (800).

We created a DataFrame `best_math_schools`, containing the **school_name** and **average_math** columns, and sorted the schools by **average_math** in descending order.

### Insights:
- **Stuyvesant High School** stands out with the highest math score, achieving an average of 780, nearly perfect.
- Many of the top-performing schools have **average math scores well above 700**, suggesting a highly competitive environment in math for top-tier schools in NYC.
- The math results can serve as a basis for comparing overall academic performance and may highlight schools with specialized programs or better resources in math education.

![Top 10 Schools](images/top_10_SAT_schools.png)

---

### Question 2: What are the top 10 performing schools based on the combined SAT scores?
We created a new `total_SAT` column by summing the **math**, **reading**, and **writing** scores for each school, and sorted them to find the top 10 performing schools.

We saved the results as a DataFrame `top_10_schools`, including the **school_name** and **total_SAT** columns.

### Insights:
- **Stuyvesant High School** leads the top 10 schools with the highest combined SAT score of **2271**.
- The difference in SAT scores between the **top school** and the **10th-ranked school** is significant, roughly 200 points, indicating a gap between top and mid-level performers.
- These top 10 schools represent the cream of NYC’s academic performance and serve as a model for other schools seeking to improve SAT scores and overall academic outcomes.

---

### Question 3: Which single borough has the largest standard deviation in the combined SAT score?
To answer this, we calculated the **standard deviation of total_SAT** for each borough to determine where the greatest variability in SAT scores exists.

We saved the results in the DataFrame `largest_std_dev`, which contains:
- **borough**: The name of the borough with the largest standard deviation.
- **num_schools**: The number of schools in that borough.
- **average_SAT**: The mean SAT score in that borough.
- **std_SAT**: The standard deviation of SAT scores in that borough.

### Insights:
- **Manhattan** has the highest standard deviation in SAT scores, indicating a **wide disparity** in school performance.
- This suggests that while some schools in Manhattan are top performers, others are far behind, and targeted educational interventions could help reduce this variability.
- The high **standard deviation** in Manhattan reveals significant differences in the academic outcomes of its schools, despite having several top-ranking schools.

```markdown   
**Borough-Level Analysis:**
   Manhattan has the highest standard deviation in SAT scores, indicating the greatest variability among schools. Here are the borough statistics:

   | Borough    | Num Schools | Average SAT | Std Dev |
   |------------|-------------|-------------|---------|
   | Manhattan  | 89          | 1340.13     | 230.29  |

---

### Summary of Insights:
- **Question 1:** Identified the best math-performing schools based on achieving 80% of the maximum score in math.
- **Question 2:** Highlighted the top 10 schools in NYC by combined SAT scores, with Stuyvesant High School topping the list.
- **Question 3:** Revealed Manhattan as the borough with the largest variability in SAT scores, indicating significant disparities in educational outcomes among its schools.



