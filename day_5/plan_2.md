### **Day 1: NumPy - Numerical Computing in Python**
#### **Objective:** Introduce students to NumPy for numerical operations and data handling.
#### **Schedule:**
1. **Introduction to NumPy (30 min)**
   - What is NumPy? Why use it?
   - Installing NumPy (`pip install numpy`)
   - Importing and basic array creation

2. **NumPy Arrays (1 hour)**
   - Differences between Python lists and NumPy arrays
   - Creating NumPy arrays (`np.array`, `np.zeros`, `np.ones`, `np.arange`, `np.linspace`)
   - Array attributes (`shape`, `dtype`, `size`, `ndim`)

3. **Array Operations (1 hour)**
   - Indexing and slicing
   - Mathematical operations (element-wise addition, multiplication, etc.)
   - Broadcasting
   - Aggregation functions (`sum`, `mean`, `std`, `min`, `max`)

4. **Matrix Operations (45 min)**
   - Creating matrices (`np.eye`, `np.random.rand`)
   - Matrix multiplication (`dot`, `@`)
   - Transposing and reshaping

5. **Practical Exercises (45 min)**
   - Generate an array and perform operations
   - Calculate statistics on a dataset using NumPy
   - Implement a simple numerical computation task

---

### **Day 2: Pandas - Data Analysis and Manipulation**
#### **Objective:** Teach students how to manipulate and analyze structured data with Pandas.
#### **Schedule:**
1. **Introduction to Pandas (30 min)**
   - What is Pandas? Why use it?
   - Installing Pandas (`pip install pandas`)
   - Importing Pandas

2. **DataFrames and Series (1 hour)**
   - Creating Series and DataFrames from lists, dictionaries, NumPy arrays
   - Reading and writing CSV/Excel files (`pd.read_csv`, `df.to_csv`)
   - Basic attributes (`df.shape`, `df.dtypes`, `df.columns`, `df.index`)

3. **Data Selection and Filtering (1 hour)**
   - Selecting columns and rows (`loc`, `iloc`)
   - Conditional filtering (`df[df['column'] > value]`)
   - Sorting and ordering (`sort_values`, `sort_index`)

4. **Data Cleaning and Transformation (45 min)**
   - Handling missing values (`isnull`, `fillna`, `dropna`)
   - Renaming columns
   - Changing data types
   - Applying functions (`apply`, `map`)

5. **Practical Exercises (45 min)**
   - Load a dataset (CSV file)
   - Perform filtering and selection
   - Clean missing data and transform values

---

### **Day 3: Data Visualization with Matplotlib & Seaborn**
#### **Objective:** Teach students how to visualize data using Python.
#### **Schedule:**
1. **Introduction to Data Visualization (30 min)**
   - Why visualization is important?
   - Matplotlib vs Seaborn vs Plotly

2. **Matplotlib Basics (1 hour)**
   - Line plots (`plt.plot`)
   - Bar charts (`plt.bar`)
   - Scatter plots (`plt.scatter`)
   - Customizing plots (titles, labels, legends, colors)

3. **Seaborn Basics (1 hour)**
   - Installing and importing Seaborn (`pip install seaborn`)
   - Creating attractive plots (`sns.barplot`, `sns.lineplot`, `sns.scatterplot`)
   - Heatmaps and correlation matrices

4. **Advanced Visualization (45 min)**
   - Histograms and distributions
   - Box plots for outlier detection
   - Pair plots for exploring relationships

5. **Practical Exercises (45 min)**
   - Load a dataset
   - Create different types of visualizations
   - Interpret and present insights from charts

---

### **Day 4: Final Project - Data Analysis & Visualization**
#### **Objective:** Apply everything learned in a hands-on project.
#### **Schedule:**
1. **Project Overview (30 min)**
   - Choose a dataset (suggested: COVID-19 cases, Titanic dataset, stock prices, or student marks)
   - Define objectives (e.g., trends, comparisons, predictions)

2. **Data Loading and Preprocessing (1 hour)**
   - Load dataset using Pandas
   - Clean missing values
   - Transform data if needed

3. **Exploratory Data Analysis (1 hour)**
   - Calculate summary statistics
   - Filter and group data
   - Find insights

4. **Data Visualization (1 hour)**
   - Create at least 3 meaningful plots
   - Customize and label plots for better understanding

5. **Presentation & Discussion (30 min)**
   - Each student/team presents findings
   - Discuss key takeaways
   - Q&A and wrap-up