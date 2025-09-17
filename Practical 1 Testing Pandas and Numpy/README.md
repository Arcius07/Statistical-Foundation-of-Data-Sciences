# **Practical 1**  - Testing Pandas and Numpy

## 🛠️ Instructions
- A **synthetic dataset** was created with some `NaN` values to simulate real-world scenarios.  
- A **random seed = 42** was set at the beginning for reproducibility.  
- While solving, `NaN` values were handled carefully (ignored or imputed, but not by dropping entire rows unnecessarily).  

---

## 📝 Practical 1 – Problems & Solutions  

### **Problem 1: Mean, Median, Age-weighted Mean**
- Constructed a synthetic dataset containing Age and Income columns, including some NaN entries.
- Applied pandas.DataFrame.mean() and median() to compute the mean and median, ensuring NaN values were ignored.
- Calculated the age-weighted mean income using numpy.average(income, weights=age) after filtering out missing values.
- Explanation included: A weighted mean is more appropriate when certain observations should have greater influence—for instance, assigning higher weight to older individuals when studying income patterns.
---

### Problem 2: Standardization (z-score) & Outliers

**How I did it:**

- First, I calculated the **mean** and **standard deviation** of the `Income` column while ignoring `NaN` values:
Then, I computed the z-scores for each value in the Salary column using the formula:
                z= (x-𝜇)/σ          	​
- Counted outliers using the rule `|z| > 3`.  
- Ensured no unnecessary row deletions by using `dropna()` only on relevant columns.  
---

### **Problem 3: Age Bins & Group Statistics**
- Defined age intervals [18–25), [25–35), [35–45), [45–60) using pandas.cut().
- Grouped the data by these age ranges with groupby().
- For each range, calculated:
   - Number of entries (count())
   - Average income (mean())
   - Median income (median())

Organized the output into a clean DataFrame and ordered it by age group.
---

### **Problem 4: Multi-dimensional Array Operations**
- Created a **2D NumPy array**.  
- Showcased:  
  - **Shape and Resize** → `array.shape`, `array.size`, `array.T` (transpose), and `flatten()`.  
  - **Negative Indexing** → Demonstrated how `array[-1]` works and intentionally caused an error using invalid slicing.  
  - **Arithmetic Operations** → Showed broadcasting (adding scalar to array) and dot product (`np.dot()`).  
  - **Linear Algebra** → Used `numpy.linalg.det()` for determinant and `numpy.linalg.inv()` for inverse.  

---

## 🛠️ Tech Stack
- **Python**  
  - NumPy  
  - Pandas  

---

## 🚀 How to Run
1. **Clone the repository**
   ```bash
   git clone https://github.com/Arcius07/Statistical-Foundation-of-Data-Sciences.git
2. **Navigate into the project folder**
   ```bash
   cd Statistical-Foundation-of-Data-Sciences
3. **Open the desired practical notebook**
   Using Jupyter Notebook:
   ```bash
   jupyter notebook
Then open the notebook manually, e.g.
Practical 1 Testing Pandas and Numpy/Pr_1.ipynb

Using Google Colab:
Upload the .ipynb file from the folder into Colab and run it there.

4. **Install required Python libraries (if not already installed)**
   ```bash
   pip install numpy pandas scipy matplotlib seaborn
5. **Run the cells in the notebook to explore the solutions step by step**
