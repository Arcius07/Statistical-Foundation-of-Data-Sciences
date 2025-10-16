🎓 Teachers Rating Dataset Analysis
🧭 Objective

The purpose of this practical exercise is to analyze a dataset of university instructors’ ratings using Python libraries such as NumPy, pandas, and SciPy.
The goal is to perform statistical analyses, conduct hypothesis testing, calculate correlations, and interpret the relationships between various factors influencing teaching evaluations.

📊 Dataset Description

The dataset contains information about university instructors and their teaching evaluation ratings.
It includes the following variables: professor name, gender, tenure status, beauty score, teaching evaluation rating, number of students in class, age, and course division (lower or upper).

Each record represents a course taught by an instructor. The beauty score and number of students columns contain some outliers, while the rating column represents the overall evaluation of teaching performance on a scale from 1 to 5.

This dataset is synthetic and has been designed purely for statistical analysis practice.

⚙️ Tools Used

The analysis was conducted using Python 3.x, with the help of libraries such as NumPy, pandas, and SciPy. The work was carried out in a Jupyter Notebook (or Google Colab) environment for interactive analysis.

🧾 Results Summary

For the T-Test, the analysis showed that gender does not have a significant impact on teaching evaluation ratings. The p-value was greater than 0.05, leading to a failure to reject the null hypothesis. This means there is no meaningful difference in average evaluation scores between male and female instructors.

In the ANOVA test, beauty scores were compared across different age groups. The results indicated no significant variation in beauty scores by age, suggesting that instructors’ attractiveness ratings remain statistically similar regardless of age group.

The Chi-Square test was used to check whether there was an association between tenure and gender. The result showed no significant relationship, meaning tenure status and gender appear to be independent of each other.

Finally, a correlation analysis between teaching evaluation scores and beauty scores revealed no significant relationship. The correlation coefficient was slightly negative, indicating a weak and non-significant trend where higher beauty scores are very slightly associated with lower evaluation scores, but not in a meaningful way.

🧩 Conclusion

Overall, the statistical tests demonstrate that there are no significant relationships among the studied variables. Gender, age, and tenure do not show measurable effects on evaluation or beauty scores. Similarly, the correlation between beauty and teaching evaluation is weak and statistically insignificant.

These findings suggest that, in this dataset, factors such as appearance, gender, and age do not play a major role in determining teaching evaluation outcomes.
