# Day-3 | Keywords, Variables & Best Practices | Global vs Local


## **1. Introduction**

- Python programs rely on **keywords** and **variables** to define logic.
- Today’s focus:
  - Understanding **keywords** in Python.
  - Learning **variables** and their scope (Global vs Local).
  - Following best practices for **naming variables**.

------

## **2. Python Keywords**

### **What are Keywords?**

- Keywords are **reserved words** in Python that have **special meaning**.
- They **cannot** be used as variable names or function names.

### **Commonly Used Keywords in Python**

1. **Conditional Statements**: `if`, `elif`, `else` 
   - [Python If ... Else](https://www.w3schools.com/python/python_conditions.asp)
2. **Loops**: `for`, `while` 
   - [Python For Loops](https://www.w3schools.com/python/python_for_loops.asp)
3. **Exception Handling**: `try`, `except`, `finally`, `raise`
   - [Python Try Except](https://www.w3schools.com/python/python_try_except.asp)
   - [Python Built-in Exceptions](https://www.w3schools.com/python/python_ref_exceptions.asp)
4. **Functions**: `def`, `return` 
   - [Python return Keyword](https://www.w3schools.com/python/ref_keyword_return.asp)
   - [Python Functions](https://www.w3schools.com/python/python_functions.asp)
5. **Classes and Modules**: `class`, `import`, `from`
   - [Python Classes and Objects](https://www.w3schools.com/python/python_classes.asp)
   - [Python Modules](https://www.w3schools.com/python/python_modules.asp)
6. **Boolean & Null Values**: `True`, `False`, `None`
7. **Operators**: `and`, `or`, `not`
   - [Python Operators](https://www.w3schools.com/python/python_operators.asp)
8. **Scope & Variables**: `global`, `nonlocal`
   - [Python - Global Variables](https://www.w3schools.com/python/python_variables_global.asp)

### **Importance of Keywords**

- Keywords help define **control flow, conditions, and function definitions**.
- Every Python program **must** use keywords to execute logic.

------

## **3. Variables in Python**

### **What is a Variable?**

- A **variable** is a container for storing data.

- Python allows 

  dynamically typed variables, meaning:
  - You don’t need to declare the type explicitly.
  - The type is inferred from the assigned value.

> **Example: Creating Variables**

```
name = "apple"  # String variable
age = 30  # Integer variable
pi = 3.14159  # Float variable
```

### **Advantages of Using Variables**

1. **Avoid Hardcoding**:
   - Instead of writing `"apple"` multiple times in a program, store it in a variable.
   - Easier to update values globally.
2. **Improve Code Maintainability**:
   - Variables make code **readable** and **modifiable**.
3. **Reduce Errors**:
   - Changing a variable **once** updates it **everywhere** in the code.

> **Example: Using Variables in a Program**

```
instance_name = "Project_XYZ"
print(instance_name)  # Output: Project_XYZ
```

------

## **4. Scope of Variables (Global vs Local)**

### **Global Variables**

- Defined **outside** of functions.
- Can be **accessed anywhere** in the program.
- Used when **multiple functions** need the same data.

> **Example: Global Variable**

```
x = 10  # Global variable

def add():
    print(x + 5)  # Accessible inside the function

add()  # Output: 15
```

### **Local Variables**

- Defined **inside** a function.
- Can **only** be used within that function.

> **Example: Local Variable**

```
def multiply():
    y = 5  # Local variable
    print(y * 2)

multiply()  # Output: 10
print(y)  # ERROR: 'y' is not defined outside the function
```

### **Global Keyword**

- Used to modify a **global variable inside a function**.

> **Example: Using `global` Keyword**

```
x = 10

def update_x():
    global x
    x = 20  # Changing global variable
    print("Updated x:", x)

update_x()  # Output: Updated x: 20
```

------

## **5. Best Practices for Naming Variables**

### **1. Use Descriptive Variable Names**

- Bad:

  ```
  n = "John"
  ```

- Good:

  ```
  full_name = "John Doe"
  ```

### **2. Use Lowercase for Variable Names**

- **Bad:** `NAME = "Alice"`
- **Good:** `name = "Alice"`

### **3. Use Snake Case or Camel Case**

- Snake Case (Recommended in Python):

  ```
  ec2_instance_name = "AWS-Server"  # Uses underscores
  ```

- Camel Case (Used in some projects):

  ```
  ec2InstanceName = "AWS-Server"  # Capitalize each word except the first
  ```

### **4. Avoid Single-Letter Variables (Except in Loops)**

- **Bad:** `x = "Project"`
- **Good:** `project_name = "Project"`

### **5. Follow Naming Conventions in Loops**

- Correct Usage of Short Names in Loops:

  ```
  for i in range(5):
      print(i)  # 'i' is commonly used in loops
  ```

------

## **6. Summary**

| Concept              | Key Points                                                   |
| -------------------- | ------------------------------------------------------------ |
| **Keywords**         | Reserved words in Python, cannot be used as variable names   |
| **Variables**        | Containers for storing data, dynamically typed in Python     |
| **Global Variables** | Declared outside functions, accessible everywhere            |
| **Local Variables**  | Declared inside functions, accessible only within the function |
| **Best Practices**   | Use lowercase, snake_case, and descriptive names             |