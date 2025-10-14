# 🎓 Student Rating Dataset Analysis

## 🧭 Objective
The aim of this practical is to analyze a **Student Rating Dataset** using Python libraries such as **NumPy**, **pandas**, and **Matplotlib**.  
The task includes performing statistical analysis, data visualization, and interpretation of various factors influencing teaching evaluations — including **tenure status**, **age**, **gender**, and **minority representation**.

---

## 📊 Dataset Description

The dataset contains information about **university professors** and their **student evaluation ratings**.  
Each record represents one professor along with demographic and professional details.

| Column | Description |
|---------|--------------|
| **prof** | Unique identifier for each professor |
| **age** | Age of the professor in years |
| **gender** | Gender of the professor (Male/Female) |
| **minority** | Indicates whether the professor belongs to a visible minority group (Yes/No) |
| **tenure** | Tenure status of the professor — whether they are tenured (Yes) or not (No) |
| **eval** | Evaluation score given by students (typically on a 1–5 scale) |
| **students** | Number of students who rated the professor |
| **beauty** | Perceived beauty score of the professor (numerical rating) |
| **division** | Course level taught by the professor (Lower or Upper division) |

---

## 🧰 Tools & Libraries Used

| Tool/Library | Purpose |
|---------------|----------|
| **Python (v3.x)** | Core programming language used for analysis |
| **pandas** | Data loading, cleaning, and manipulation |
| **NumPy** | Numerical computations and descriptive statistics |
| **Matplotlib (Pyplot)** | Visualization of data distributions and categorical variables |
| **Seaborn** | Enhanced plotting and styling of graphs |
| **Google Colab** | Interactive environment for coding and visualization |

---

## 🧾 Results Summary

1. Tenure Status and Visible Minority
The analysis investigated whether tenure status differed based on being a visible minority.

For professors identified as a visible minority, 65.6% were tenured.

For professors not identified as a visible minority, 61.8% were tenured.

Finding: The percentages are very close, suggesting that in this dataset, there is no strong evidence that tenure status differs based on being a visible minority.

2. Age and Tenure
The average age and its variability were compared between tenured and untenured professors.

Tenured Professors: The mean age was 52.3 years with a standard deviation of approximately 11.0.

Untenured Professors: The mean age was 51.4 years with a standard deviation of approximately 11.4.

Finding: Tenured professors are, on average, slightly older, which is expected since tenure is typically awarded after years of service. The age variation within both groups is similar.

3. Visualizing the Age Distribution
A histogram and a boxplot were created to visualize the Age variable. The histogram was determined to be more effective as it clearly shows the frequency and distribution of professors across different age groups.

4. Bar Charts for Categorical Data
The difference between vertical (pyplot.bar) and horizontal (pyplot.barh) bar charts was defined. A vertical bar chart was then plotted to show the count of professors by gender, effectively visualizing the categorical data.

5. Median Evaluation Score for Tenured Professors
The central tendency of student ratings for tenured faculty was calculated.

Finding: The median evaluation score for tenured professors is 3.25.

---
