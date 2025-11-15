🌸 Iris Dataset — KNN Classification Analysis
🧭 Objective

The goal of this practical is to apply the K-Nearest Neighbors (KNN) algorithm on the Iris dataset to classify flower species.
This experiment includes:

Exploratory Data Analysis (EDA)

Feature Scaling

Model Training

Error Rate Comparison

Selecting the Best K

Model Evaluation & Visualization

This practical helps understand how distance-based classification works in machine learning.

📊 Dataset Description

The Iris dataset contains measurements of 150 iris flowers belonging to three different species.

📁 Columns Description
Column	Description
sepal length (cm)	Length of the sepal
sepal width (cm)	Width of the sepal
petal length (cm)	Length of the petal
petal width (cm)	Width of the petal
species	Target variable: Setosa, Versicolor, Virginica
🧰 Tools & Libraries Used
Tool / Library	Purpose
Python (3.x)	Programming environment
pandas	Data loading & EDA
NumPy	Numerical operations
scikit-learn	KNN model, scaling, metrics
Matplotlib	Graph plotting
Jupyter Notebook / Google Colab	Code execution
🧪 Procedures & Results
1️⃣ Exploratory Data Analysis (EDA)

Performed using:

head() → Preview dataset

describe() → Summary statistics

groupby() → Group statistics by species

This helps to understand feature distribution and species differences.

2️⃣ Feature Scaling

Used StandardScaler to normalize numerical features.
Scaling is crucial because KNN relies on distance measurements.

3️⃣ Train-Test Split & KNN Model Training

Dataset split → 70% training, 30% testing

Initial model trained with K = 5

4️⃣ Confusion Matrix & Accuracy Score

After prediction:

Confusion matrix shows classification performance

Accuracy score confirms high model performance (typically >95%)

5️⃣ Classification Report

Includes:

Precision

Recall

F1-score

All three species achieve high performance due to Iris’ clean separation.

6️⃣ Error Rate Comparison for K = 1 to 20

K values from 1 to 20 were tested to observe how error changes.
This helps determine the most stable and accurate K value.

7️⃣ Plot: Error Rate vs K Values

A line plot was created to visualize:

Error patterns

Which K values perform best

Overfitting at lower K values

Stability at higher K values

8️⃣ Finding the Best K

Best K = value with minimum error rate
Usually found around K = 3–7 for the Iris dataset.

9️⃣ Visualization of Results (PCA)

Dimensionality reduction using PCA (2 components) was performed to plot:

Points colored by species

Clear separation between Setosa, Versicolor, Virginica

📈 Summary of Findings
Step	Purpose	Result
EDA	Understand dataset	Clear differences between species
Scaling	Normalize features	Essential for KNN
Model Training	Fit KNN	Initial K=5 performed well
Confusion Matrix	Evaluate predictions	Very high accuracy
Error Rate Analysis	Find optimal K	Best K around 3–7
PCA Visualization	Show class clusters	Species visually separable
🏁 Conclusion

This practical provided hands-on experience in:

✔ Performing KNN classification
✔ Understanding the need for feature scaling
✔ Evaluating model performance
✔ Testing multiple K values to find the optimal one
✔ Visualizing high-dimensional data using PCA

Key Insights

KNN performs extremely well on the Iris dataset due to its natural class separation.

Choosing an optimal K is important for reducing error and improving accuracy.

Visualization techniques like PCA help understand dataset structure.
