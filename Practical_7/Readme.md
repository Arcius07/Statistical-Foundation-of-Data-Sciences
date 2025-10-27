🎓 Teachers Rating Dataset Analysis
🧭 Objective

The aim of this practical is to explore relationships and differences within the Teachers’ Rating Dataset using regression analysis, ANOVA, and correlation tests.
These experiments help determine how factors such as gender, beauty, and age influence teaching evaluation scores.
Statistical methods are implemented using Python for meaningful interpretation.

📊 Dataset Description

The dataset named ratings contains data about university professors and their corresponding teaching evaluation ratings.
It includes demographic and professional details of instructors.

Column	Description
Prof	Professor’s name or unique identifier
Gender	Gender of the professor (Male/Female)
Tenure	Indicates whether the professor is tenured (Yes/No)
Beauty	Numerical score representing the perceived beauty of the professor
Evaluation	Teaching evaluation score given by students
Students	Number of students who rated the professor
Age	Age of the professor in years
CourseLevel	Course type — Lower or Upper division
🧰 Tools & Libraries Used
Tool/Library	Purpose
Python (v3.x)	Programming environment
pandas	Data manipulation and preprocessing
NumPy	Numerical and statistical computations
statsmodels	Regression, T-test, and ANOVA analysis
scipy	Statistical hypothesis testing and correlation
Matplotlib / Seaborn	Data visualization
Google Colab / Jupyter Notebook	Code execution and visualization environment
🧪 Statistical Analyses & Results
1️⃣ Gender-based Regression

Model: Evaluation ~ Gender
Based on the regression results (F(1,118) = 5.27, p = 0.0235), there is a statistically significant difference in teaching evaluation ratings between male and female instructors.
On average, male instructors scored about 0.24 points higher than female instructors.
This suggests a real gender effect, though modest in size.

2️⃣ ANOVA — Beauty by Age Group

Model: Beauty ~ age_group
The ANOVA test results were not statistically significant, F(4,116) = 0.68, p = 0.567.
This indicates that instructors’ beauty scores do not significantly differ across age groups.

3️⃣ Regression — Beauty Predicting Evaluation

Model: Evaluation ~ Beauty
The regression was statistically significant, F(1,118) = 4.09, p = 0.045, with R² = 0.033.
Beauty had a small but negative effect on evaluation ratings (β = -0.159, p = 0.045).
This means that as instructors’ beauty scores increased, their teaching evaluations slightly decreased.
However, the model explains only 3.3% of the variance, indicating a very small practical impact.

📈 Summary of Findings
Analysis	Variable(s)	Result	Interpretation
Regression (Gender vs Evaluation)	Gender	Significant (p = 0.0235)	Male instructors scored higher on average
ANOVA (Beauty vs Age Group)	Beauty, Age	Not Significant (p = 0.567)	Beauty does not vary by age
Regression (Beauty vs Evaluation)	Beauty	Significant (p = 0.045)	Beauty slightly decreases evaluation ratings
🏁 Conclusion

This practical provided hands-on experience in:

Performing regression analysis and interpreting coefficients and significance levels.

Conducting ANOVA to compare group means.

Exploring relationships between variables through statistical modeling.

Key insights include:

Gender shows a small but significant effect on evaluation ratings.

Beauty varies little with age and has a negative association with teaching evaluations.

Overall, demographic features explain only a small portion of variation in student ratings, suggesting that other factors (like teaching style or subject difficulty) may play a larger role.
