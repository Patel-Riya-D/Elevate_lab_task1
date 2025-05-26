# 🚢 Elevate Lab - Task 1: Data Cleaning & Preprocessing

## 🧠 Objective
Prepare the Titanic dataset for machine learning by handling missing values, encoding categorical variables, scaling features, and removing outliers to improve data quality and model performance.

---

## 🛠️ Tools Used
- **Python** 🐍  
- **Pandas** – for data loading and cleaning  
- **NumPy** – for numerical operations  
- **Matplotlib & Seaborn** – for visualizations  
- **Scikit-learn** – for preprocessing and scaling  
- **SciPy** – for outlier detection (Z-score)

---

## ✅ What I Did

### 1. 📂 Data Loading & Exploration
- Loaded the Titanic dataset using `pandas.read_csv()`.
- Explored the structure with `.info()`, `.describe()`, and `.isnull().sum()`.

### 2. 🧼 Missing Value Handling
- Filled missing values in the `Age` column with the mean.
- Filled missing values in the `Embarked` column with the mode.
- Dropped the `Cabin` column due to excessive missing values.

### 3. 🧠 Categorical Encoding
- Applied **One-Hot Encoding** using `pd.get_dummies()` to convert categorical features like `Sex`, `Embarked`, and `Pclass` into numeric format.

### 4. 📊 Feature Scaling
- Scaled numerical columns (`Age`, `Fare`) using `StandardScaler` to standardize feature ranges.

### 5. 🚨 Outlier Detection & Removal
- Used the **Z-score method** from `scipy.stats` to detect and remove statistical outliers (Z-score > 3 or < -3) from the scaled numerical columns.

### 6. 📈 Data Visualization
- Plotted **boxplots** to visualize outliers in numeric features.
- Created a **heatmap** of feature correlations to better understand data relationships.

- ### 🔹 Boxplot of Scaled Features: Age and Fare

![Boxplot of Age and Fare] ![image](https://github.com/user-attachments/assets/f84c7485-3ea2-42b3-af20-5e1323f35c50)


- Visualizes the distribution of `Age` and `Fare` after scaling.
- Outliers appear as dots beyond the whiskers.
- `Fare` shows more extreme outliers than `Age`.
- Helped identify and justify the need for **outlier removal using Z-score**.

---

### 🔹 Correlation Heatmap (After Cleaning) 

![Correlation Heatmap] ![image](https://github.com/user-attachments/assets/e0edcecf-f8b3-4e6a-91d8-75e0b008a3af)


- Shows correlation between all features after preprocessing.
- Highlights useful patterns:
  - Negative correlation between `Sex_male` and `Survived`
  - Positive correlation between `Fare` and `Survived`
  - Insightful feature relationships for future model selection

---

## 📈 Outcome
- The final dataset is:
  - Cleaned and preprocessed
  - Encoded and scaled
  - Free from significant outliers
- ✅ Ready for use in predictive modeling and machine learning pipelines.

---

## 📁 Dataset Source
- [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic)


