# Task 1: Exploring and Visualizing the Iris Dataset

## Objective

The objective of this task is to explore and visualize a simple dataset to understand its structure, feature distributions, and relationships between variables using Python data analysis and visualization libraries.

---

## Dataset Used

**Iris Dataset**

The Iris dataset is a classic dataset in data science and machine learning. It contains 150 samples of iris flowers divided into three species:

- Setosa
- Versicolor
- Virginica

Each sample includes four numerical features:

- Sepal Length (cm)
- Sepal Width (cm)
- Petal Length (cm)
- Petal Width (cm)

The dataset was loaded in CSV format using pandas (via seaborn/sklearn source).

---

## Tools and Libraries Used

- Python
- Pandas (data loading and inspection)
- NumPy
- Matplotlib (data visualization)
- Seaborn (statistical visualization)

---

## Steps Performed

### 1️⃣ Data Loading
- Loaded the dataset into a pandas DataFrame.
- Verified successful loading of data.

### 2️⃣ Data Inspection
- Checked dataset shape using `.shape`
- Viewed column names
- Displayed first few rows using `.head()`
- Used `.info()` to inspect data types and missing values
- Used `.describe()` to generate summary statistics

### 3️⃣ Data Visualization

#### ✔ Scatter Plot
- Visualized relationships between features (e.g., Sepal Length vs Sepal Width).
- Used color coding to differentiate species.
- Helped identify class separability.

#### ✔ Histograms
- Displayed distribution of each numerical feature.
- Observed spread, skewness, and value concentration.

#### ✔ Box Plots
- Identified data spread and potential outliers.
- Compared feature ranges across measurements.

---

## Key Observations

- The dataset contains 150 samples and 4 numerical features.
- No missing values were found.
- Petal Length and Petal Width show strong separation between species.
- Setosa species is clearly distinguishable from the other two.
- Data distributions appear relatively balanced across features.

---

## Skills Demonstrated

- Data loading and preprocessing using pandas
- Exploratory Data Analysis (EDA)
- Descriptive statistical analysis
- Data visualization using matplotlib and seaborn
- Interpretation of feature relationships and distributions

---

## Conclusion

This task provided foundational experience in data exploration and visualization. Understanding dataset structure and feature behavior is a critical first step before applying machine learning models. The Iris dataset serves as an ideal example for practicing exploratory data analysis techniques.
