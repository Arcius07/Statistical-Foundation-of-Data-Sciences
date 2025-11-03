# 🧠 Decision Tree Classifier – Pima Indian Diabetes Dataset

## 🎯 Aim
To build and visualize a **Decision Tree Classifier** using the **Pima Indian Diabetes Dataset** (from Kaggle) and compute **Entropy**, **Information Gain**, and **Gini Index** to determine the best root node.

---

## 📚 Dataset
**Source:** [Pima Indians Diabetes Database on Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

The dataset contains diagnostic measurements of Pima Indian women aged 21 and above.  
Each record represents whether the patient has diabetes (1) or not (0).

**Columns:**
- Pregnancies  
- Glucose  
- BloodPressure  
- SkinThickness  
- Insulin  
- BMI  
- DiabetesPedigreeFunction  
- Age  
- Outcome (Target Variable)

---

## ⚙️ Steps Performed

### 1️⃣ Import Required Libraries
Loaded Python libraries such as pandas, NumPy, matplotlib, and Scikit-learn.

### 2️⃣ Load Dataset
Read `diabetes.csv` file into a DataFrame.

### 3️⃣ Feature Selection
Separated **independent features (X)** and **dependent target (y)**.

### 4️⃣ Split Dataset
Divided data into **training (80%)** and **testing (20%)** subsets using `train_test_split()`.

### 5️⃣ Build Decision Tree Models
Built two models using different criteria:
- **Criterion = Gini**
- **Criterion = Entropy**

### 6️⃣ Evaluate Models
Calculated and compared accuracy of both models on the test dataset.

### 7️⃣ Visualize Decision Tree
Used `plot_tree()` to visualize the structure of both decision trees.

### 8️⃣ Extract Decision Rules
Used `export_text()` to print readable rules from the trained model.

### 9️⃣ Compute Entropy, Information Gain, and Gini Index
Manually calculated these metrics for the **Glucose** feature to show how the tree selects the root node.

---

## 📈 Results

| Metric | Criterion = Gini | Criterion = Entropy |
|:-------:|:----------------:|:-------------------:|
| Accuracy | ~0.73 (approx) | ~0.74 (approx) |

- **Root Node Selected:** Glucose  
- **Reason:** Highest Information Gain and Lowest Gini Impurity.

---

## 🧮 Key Formulas

- **Entropy (S):**  
  \[
  Entropy(S) = -\sum p_i \log_2(p_i)
  \]

- **Information Gain (IG):**  
  \[
  IG(S, A) = Entropy(S) - \sum \frac{|S_v|}{|S|} Entropy(S_v)
  \]

- **Gini Index:**  
  \[
  Gini = 1 - \sum p_i^2
  \]

---

## 🖼️ Visual Output
Two decision tree visualizations are generated:
- Decision Tree (Criterion = Gini)
- Decision Tree (Criterion = Entropy)

Both highlight **Glucose** as the primary decision factor.

---

## ✅ Conclusion
- Decision Trees are intuitive and interpretable classification models.  
- The **Glucose** feature gives the **highest Information Gain**, making it the **best root node**.  
- Both **Gini** and **Entropy** criteria perform similarly, with slight variations in accuracy and splits.  
- Visualization helps understand decision-making paths of the model clearly.

---

## 💻 Technologies Used
- Python 3.x  
- Pandas  
- NumPy  
- Matplotlib  
- Scikit-learn

---
