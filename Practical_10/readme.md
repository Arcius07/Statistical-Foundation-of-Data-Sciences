🍷 Wine Dataset Analysis (Python)

This project performs Exploratory Data Analysis, Visualization, Feature Scaling, and PCA on the popular Wine Dataset from sklearn.

It is designed as a complete practical assignment for data preprocessing and dimensionality reduction.

📌 Features Covered

✔️ Basic Statistics (describe())

✔️ Boxplot by Class Labels

✔️ Scatterplot using Two Variables

✔️ Covariance Matrix Heatmap

✔️ Feature Scaling using StandardScaler

✔️ PCA for Class Separation

📂 Project Structure

Wine-Analysis/

│

├── wine_analysis.py

└── README.md

🔧 Installation

# Clone the repository

git clone https://github.com/<your-username>/Wine-Analysis.git

# Navigate into the project folder

cd Wine-Analysis

# Install dependencies

pip install numpy pandas matplotlib seaborn scikit-learn

▶️ How to Run

python wine_analysis.py

📊 Outputs Produced

1️⃣ Basic Statistics

Summary of mean, std deviation, min–max, and quartiles.

2️⃣ Boxplot

Visualizes alcohol content across wine classes.

3️⃣ Scatterplot

Plots color_intensity vs hue with color-coded classes.

4️⃣ Covariance Matrix

Generates a heatmap showing feature correlations.

5️⃣ Scaled Dataset

Data normalized using StandardScaler.

6️⃣ PCA Visualization

Shows 2D projection with clear class separation.

📦 Libraries Used

numpy

pandas

matplotlib

seaborn

sklearn.preprocessing.StandardScaler

sklearn.decomposition.PCA

📚 Dataset Information

The Wine dataset contains:

13 numerical chemical properties

3 wine classes

178 samples
