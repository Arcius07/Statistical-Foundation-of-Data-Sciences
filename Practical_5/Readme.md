# 🎓 Teachers Rating Dataset Analysis

## 🧭 Objective
The aim of this practical is to perform **probability and hypothesis testing** using the **Teachers’ Rating Dataset**.  
The practical focuses on calculating probabilities of evaluation scores and conducting a **two-tailed hypothesis test** based on a normal distribution.  
Python libraries such as **NumPy**, **pandas** were used to perform computations.

---

## 📊 Dataset Description

The dataset named **`ratings`** contains information about **university professors** and their corresponding teaching evaluation ratings.  
It includes demographic details and professional attributes related to the instructors.

| Column | Description |
|---------|--------------|
| **Prof** | Professor’s name or unique identifier (duplicates may occur for multiple courses) |
| **Gender** | Gender of the professor (Male/Female) |
| **Tenure** | Indicates whether the professor is tenured (Yes) or untenured (No) |
| **Beauty** | Numerical score representing the perceived beauty of the professor |
| **Rating** | Teaching evaluation score given by students (typically on a 1–5 scale) |
| **Students** | Number of students who participated in the evaluation |
| **Age** | Age of the professor in years |
| **Division** | Indicates whether the course taught was a lower-division or upper-division course |

---

## 🧰 Tools & Libraries Used

| Tool/Library | Purpose |
|---------------|----------|
| **Python (v3.x)** | Programming environment for analysis |
| **pandas** | Data manipulation and statistical calculations |
| **NumPy** | Numerical operations and probability computations |
| **Matplotlib** | Data visualization and plotting |
| **Google Colab** | Environment for executing code and displaying results |

---

## 🧾 Results Summary

Descriptive statistics for the eval score were calculated, finding a population mean of 3.99 and a standard deviation of 0.55.

The probability of a professor receiving an evaluation score greater than 4.5 was computed to be approximately 18.2%.

The probability of a professor's score falling between 3.5 and 4.2 was calculated to be 62.5%.

A two-tailed z-test was performed on a random sample of 30 evaluation scores. The test yielded a z-statistic of -0.82 and a p-value of 0.41. Since the p-value is greater than the significance level (α = 0.05), the null hypothesis was not rejected, indicating no significant difference between the sample mean and the population mean.

🏁 Conclusion
This practical successfully demonstrated the application of probability theory and inferential statistics to a real-world dataset using Python. Through this analysis, I have learned how to:

Calculate probabilities for a normally distributed variable using its mean and standard deviation.

Formulate a hypothesis and conduct a two-tailed z-test to compare a sample mean to a population mean.

Interpret the z-statistic and p-value to make a statistically sound conclusion about the hypothesis.
