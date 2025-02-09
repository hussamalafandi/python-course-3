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