# Exploratory Data Analysis (EDA) Steps

## Overview
The Netflix dataset contains information about movies and TV shows available on the platform, including details like titles, genres, ratings, release years, and more. Exploratory Data Analysis (EDA) on this dataset helps to uncover patterns such as the most popular genres, the distribution of ratings, the correlation between release years and ratings, or trends over time. By performing EDA, we can gain valuable insights into user preferences, content trends, and distribution of features like genre and content type, which are essential for decision-making and recommendations.
## Steps for EDA

## <span style="color:green">Using</span>

## 1. Pandas
- **Purpose**: Data manipulation and analysis.
- **Functions for EDA**:
  - `df.describe()`: Summary statistics.
  - `df.info()`: Data types and missing values.
  - `df.isnull().sum()`: Count missing values.
  - `df.corr()`: Correlation matrix.
- **Installation**: `pip install pandas`

## 2. NumPy
- **Purpose**: Numerical operations.
- **Functions for EDA**:
  - `np.mean()`,`np.median()`, `np.std()`: Calculate basic statistics.
- **Installation**: `pip install numpy`

## 3. Matplotlib
- **Purpose**: creating static, interactive, and publication-quality visualizations.
- **Functions for EDA**:
  - `plt.plot()`: Create line plots.
  - `plt.bar()`: create bar charts.
  - `plt.pie()`: create pie charts.
  - `plt.hist()`: Create histograms.
  - `plt.title()`, `plt.xlabel()`, `plt.ylabel()`: Customize chart titles and axis labels.
  - **Installation**: `pip install matplotlib`

    
## 4. Seaborn
- **Purpose**: Statistical data visualization.
- **Functions for EDA**:
  - `sns.heatmap()`: Correlation heatmaps.
  - `sns.boxplot()`: Box plots.
  - `sns.jointplot()`: Check correlation between two variables.
  - `sns.lineplot()`: Draw lineplot.
- **Installation**: `pip install seaborn

## 5. Plotly
-  **Purpose**: Interactive plotting library for creating web-based, dynamic visualizations.
-  **Functions for EDA**:
   - `go.Figure()`: Create figures for custom visualizations.
   - `px.choropleth()`: Plotly function used to create geographic choropleth maps.
   - `update_layout()`: Customize plot appearance and layout.
- **Installation**: `pip install plotly`

## 6. import warnings
 - **it helps suppress unnecessary warnings to keep the analysis output clean and focused.**



````````````````````````````````````````````````````````````````````````````````````````````

Explain:
1. Load the Dataset
python
import pandas as pd

df = pd.read_csv('netflix_train.csv')
df.head()


2. Understand the Dataset
Check the number of rows and columns:
python
df.shape

Display column names:
python
df.columns

Check info and data types:
python
df.info()


3. Handle Missing Values
Check for missing values:
python
df.isnull().sum()

Fill or drop missing values if necessary:
python
df.fillna(method='ffill', inplace=True)  # Forward fill
  or
df.dropna(inplace=True)  # Remove missing values
```

4. Summary Statistics
python
df.describe()


5. Check for Duplicates
python
df.duplicated().sum()
df.drop_duplicates(inplace=True)


6. Data Visualization
a) Univariate Analysis
Histogram:
python
import matplotlib.pyplot as plt
import seaborn as sns

sns.histplot(df['column_name'], kde=True)
plt.show()


Boxplot:
python
sns.boxplot(x=df['column_name'])
plt.show()


b) Bivariate Analysis
Scatter Plot:
python
sns.scatterplot(x=df['feature1'], y=df['feature2'])
plt.show()


Correlation:
python
sns.jointplot(x='column_name1',y='column_name2',data=df])
plt.show()


7. Identify Outliers
python
sns.boxplot(x=df['column_name'])
plt.show()


8. Feature Engineering
Creating new features if necessary:
python
df['new_feature'] = df['feature1'] / df['feature2']


9. Data Transformation 
Encoding categorical variables:
python

from sklearn.preprocessing import LabelEncoder
le =  LabelEncoder()
col=["----"]
for i in col:
      df[i]=le.fit_transform(df[i])


10. More steps add in EDA(ipynb file) like Multivariant and plotly graph.
```````````````````````````````````````````````````````````````````````````````````````````````````
11. Insights

- Top 5(international movies, drama..) genres in which most content is being distributed.
- Most content release in 2018.
- According to geographical disstribution, the most content count in united states then india.
- In Time series analysis, the most titles count in 2019, month june and rating TV_MA.
- When we analyse the count of ratings , TV_MA take most count of rating.
- The length of movies or episodes mostly take 1 Season.
- The distribution of content,acording to countrywise(United states>india>united kingdom>japan>South korea).
- The time of duration according to release is reduce and rating is up year by year.
- The international movies, drama etc.genres and type Movie content are more popular among users.

10. Save Processed Data
python
df.to_csv('processed_data.csv', index=False)


````````````````````````````````````````````````````````````````````````````````````````````````
## Conclusion
These steps provide a comprehensive approach to performing EDA.


## Feedback and Contributions

We welcome contributions! If you have insights, improvements, or suggestions, please open an issue or submit a pull request.
- 🌐 [GitHub Profile](https://github.com/ShubhamKumar0786https://github.com/ShubhamKumar0786)  
- 📧 Email:shubhamkashyap9501@gmail.com
- LinkedIn: [Linkedin_link](https://www.linkedin.com/in/shubham0786/)
