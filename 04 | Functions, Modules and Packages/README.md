# **Day-4: Functions, Modules, and Packages in Python**

## **1. Introduction**

- Python provides **functions, modules, and packages** to make code **reusable, modular, and organized**.
- Why are these important for DevOps?
  - Automating tasks like AWS resource management, Jira ticket creation, and API interactions.
  - Writing structured, reusable scripts for different teams.
- Topics Covered:
  1. Functions
  2. Modules
  3. Packages
  4. Virtual Environments

------

## **2. Functions in Python**

### **What is a Function?**

- A **function** is a block of code designed to perform a specific task.
- Functions help in:
  - **Code reusability** (write once, use multiple times).
  - **Better readability** (structured code).
  - **Easy debugging** (isolating functionality).

### **Function Syntax**

```
def function_name():
    # Function logic
    return result  # Optional
```

### **Example: Basic Function**

```
def add_numbers():
    a = 5
    b = 10
    result = a + b
    print("Sum:", result)

# Calling the function
add_numbers()
```

### **Passing Arguments to Functions**

```
def add(a, b):  # Accepting parameters
    return a + b  # Returning output

result = add(10, 20)  # Calling function with arguments
print("Sum:", result)  # Output: Sum: 30
```

### **Function Advantages**

| Feature         | Benefit                         |
| --------------- | ------------------------------- |
| **Reusability** | Write once, use multiple times. |
| **Readability** | Organized, structured code.     |
| **Debugging**   | Errors can be isolated easily.  |

------

## **3. Modules in Python**

### **What is a Module?**

- A **module** is a file containing **Python functions and variables** that can be reused.
- Instead of rewriting functions, you can **import a module** and use its functions.

### **Creating a Module**

1. Create a Python file (`calculator.py`).
2. Define functions inside it.

```
# calculator.py (Module)
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

### **Using a Module in Another File**

```
# main.py (Using the module)
import calculator

result = calculator.add(10, 5)
print("Sum:", result)  # Output: Sum: 15
```

### **Importing Specific Functions**

```
from calculator import add

print(add(7, 3))  # Output: 10
```

### **Module Benefits**

- **Reusability**: Use functions from other files.
- **Code Organization**: Keep related functions together.
- **Avoids Duplication**: Write once, use everywhere.

------

## **4. Packages in Python**

### **What is a Package?**

- A **package** is a collection of modules stored in a directory.
- It must contain a special file **`__init__.py`** to be recognized as a package.

### **Creating a Package**

1. Create a directory `math_operations/`
2. Inside, create a modules (`calculator.py`, statistics.py).
3. Add an `__init__.py` file to define the package.

```
math_operations/  <-- Package
│── __init__.py   <-- Initializes the package
│── calculator.py  <-- Module inside package
│── statistics.py  <-- Module inside package

```

- [pypi](https://pypi.org/): Find, install and publish Python packages
- useful cmd:
  - `pip install <package name>`: install package
  - `pip list`: list all of pacakges

### **Using a Package**

```
# Importing a module from a package
from math_operations import calculator

print(calculator.add(5, 2))  # Output: 7
```

### **Package Benefits**

- **Organized Codebase**: Keeps modules structured.
- **Encapsulation**: Group related functionality.
- **Scalability**: Easily extendable.

------

## **5. Virtual Environments in Python**

### **What is a Virtual Environment?**

- A **virtual environment** creates **isolated Python environments**.
- logical seperation on your virtual machine for python packages
- It is useful when running different projects on the same virtual machine that require different package versions.

### **Creating a Virtual Environment**

```
# install python virtual environment
pip install virtualenv

# Create virtual environment for project a, you should be able to see projet a folder after executing the cmd
python -m venv project_a_env
```

### **Activate/ Deactivate a Virtual Environment**

- Windows:

  ```
  my_project_env\Scripts\activate
  deactivate
  ```

- Mac/Linux:

  ```
  source project_a_env/bin/activate
  deactivate
  ```

### **Why Use Virtual Environments?**

| Problem                      | Solution                               |
| ---------------------------- | -------------------------------------- |
| Conflicting package versions | Isolated environments for each project |
| Dependency management        | Each project has its own libraries     |
| Cleaner workspace            | No unnecessary global installations    |

------

## **6. Summary**

| Concept                  | Key Points                                                   |
| ------------------------ | ------------------------------------------------------------ |
| **Functions**            | Reusable blocks of code, defined using `def`.                |
| **Modules**              | Python files (`.py`) containing functions, imported using `import`. |
| **Packages**             | Collection of modules stored in directories, requires `__init__.py`. |
| **Virtual Environments** | Isolated Python workspaces, managed with `venv`.             |