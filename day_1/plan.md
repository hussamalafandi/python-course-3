### **Day 1: Setting Up Python Environments and Working with Jupyter Notebooks**  
**Objective:** Equip students with the tools to create Python environments, manage dependencies, and use Jupyter Notebooks for interactive coding.

---

### **Schedule:**
| **Time**   | **Topic**                                  | **Description**                                  |
|------------|--------------------------------------------|-------------------------------------------------|
| **9:00 - 9:30** | **Introduction to Python Environments** | Overview of environments and their importance.   |
| **9:30 - 10:15** | **Setting Up Virtual Environments**    | Hands-on: Creating and activating environments.  |
| **10:15 - 10:45** | **Managing Dependencies**             | Installing Jupyter Notebook and managing packages. |
| **10:45 - 11:15** | **Introduction to Jupyter Notebooks** | Using notebooks for coding and documentation.    |
| **11:15 - 12:00** | **Working with Jupyter Cells**        | Writing and running Python code in notebooks.    |
| **12:00 - 12:30** | **Basic Python Practice in Jupyter**  | Implement basic Python concepts in notebooks.    |
| **12:30 - 13:00** | **Q&A and Troubleshooting**           | Review and resolve setup issues.                 |

---

### **Detailed Plan**

#### **9:00 - 9:30: Introduction to Python Environments**
**Topics:**
- What are Python environments?
- Benefits of virtual environments:
  - Isolating dependencies for different projects.
  - Avoiding conflicts between installed libraries.
- Overview of `venv` and `conda`.

**Discussion:**
- Compare system Python vs. virtual environments.
- Explain the role of package managers like `pip` and `conda`.

---

#### **9:30 - 10:15: Setting Up Virtual Environments**
**Topics:**
- Creating a virtual environment:
  - Using `venv` for standard Python.
  - Using `conda` for those with Anaconda installed.
- Activating and deactivating environments.

**Hands-on Exercise:**
- Create a virtual environment with `venv`:
  ```bash
  python -m venv my_env
  source my_env/bin/activate  # Mac/Linux
  my_env\\Scripts\\activate  # Windows
  ```

- OR with `conda`:
  ```bash
  conda create --name my_env python=3.10
  conda activate my_env
  ```

- Test the environment by running:
  ```bash
  python --version
  ```

---

#### **10:15 - 10:45: Managing Dependencies**
**Topics:**
- Installing Python libraries with `pip` or `conda`.
- Managing dependencies:
  - What is `requirements.txt`?
  - How to generate and use it.

**Hands-on Exercise:**
- Install Jupyter Notebook in the virtual environment:
  ```bash
  pip install notebook
  ```
- Check installed packages:
  ```bash
  pip list
  ```

- Create a `requirements.txt` file:
  ```bash
  pip freeze > requirements.txt
  ```

---

#### **10:45 - 11:15: Introduction to Jupyter Notebooks**
**Topics:**
- What is Jupyter Notebook?
- Benefits:
  - Interactive coding.
  - Inline documentation.
  - Visualization support.
- How to launch Jupyter Notebook.

**Hands-on Exercise:**
- Launch Jupyter Notebook:
  ```bash
  jupyter notebook
  ```
- Create and rename a new notebook.

---

#### **11:15 - 12:00: Working with Jupyter Cells**
**Topics:**
- Types of cells:
  - Code cells: Running Python code.
  - Markdown cells: Writing documentation.
- Jupyter commands:
  - Running cells (`Shift + Enter`).
  - Adding/deleting cells.

**Hands-on Exercise:**
- Create a Markdown cell:
  ```markdown
  # My First Notebook
  This is a Markdown cell where I can write **formatted text**.
  ```
- Add a code cell:
  ```python
  print("Hello, Jupyter!")
  ```
- Test basic Python commands in a notebook:
  ```python
  for i in range(5):
      print(f"Number: {i}")
  ```

---

#### **12:00 - 12:30: Basic Python Practice in Jupyter**
**Topics:**
- Use Jupyter Notebooks to practice Python concepts students already know:
  - Variables, loops, and functions.

**Hands-on Exercise:**
- Write a Python function to calculate the sum of squares of a list:
  ```python
  def sum_of_squares(numbers):
      return sum([x**2 for x in numbers])

  print(sum_of_squares([1, 2, 3, 4]))
  ```
- Test a loop to print odd numbers between 1 and 10:
  ```python
  for i in range(1, 11):
      if i % 2 != 0:
          print(i)
  ```

---

#### **12:30 - 13:00: Q&A and Troubleshooting**
**Topics:**
- Address any setup issues students encountered:
  - Virtual environment activation.
  - Installing Jupyter Notebook.
  - Running notebooks.
- Recap key takeaways:
  - How to set up a virtual environment.
  - How to launch and use Jupyter Notebooks.

---

### **Homework for Day 1**
1. **Set up a new virtual environment** and activate it.
2. Install the following libraries in the environment (but don’t use them yet):
   ```bash
   pip install numpy pandas matplotlib
   ```
3. Write and test a Python script in Jupyter Notebook:
   - Define a function.
   - Use a loop to process a list.
4. Explore how Markdown cells can format text and organize notebooks.
