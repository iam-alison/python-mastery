# Ch-02 | Data Types | Strings | String Handling Functions

## **1. Introduction**

- Understanding **data types** is crucial in Python.
- Python has built-in **data types** that help the interpreter identify the type of data stored.
- In this session, we focus on **strings**, **numeric types**, and **regular expressions**.

------

## **2. Data Types in Python**

Python's data types are classified into:

1. **Numeric Data Types**:

   - `int` (Integer) → Whole numbers (e.g., `5`, `100`)
   - `float` (Floating Point) → Decimal numbers (e.g., `5.2`, `3.14`)

2. **String Data Type**:

   - Strings are sequences of characters

      enclosed in:

     - **Single quotes ('')**
     - **Double quotes ("")**
     - **Triple quotes (''' or """)** → Used for multi-line strings.

3. **Sequence Data Types**:

   - `list` → Ordered, mutable collection (e.g., `[1, 2, 3]`)
   - `tuple` → Ordered, immutable collection (e.g., `(1, 2, 3)`)

4. **Mapping Data Types**:

   - `dict` (Dictionary) → Key-value pairs (e.g., `{"name": "Alice", "age": 25}`)

5. **Set Data Types**:

   - `set` → Unordered, unique elements (e.g., `{1, 2, 3}`)

6. **Boolean Data Type**:

   - `bool` → Holds `True` or `False`.

------

## **3. How Python Determines Data Types**

- Python is **dynamically typed**, meaning **you don't need to declare data types explicitly**.

- Example:

  ```
  name = "Abhishek"   # String
  age = 25            # Integer
  pi = 3.14           # Float
  ```

------

## **4. String Handling Functions**

Python provides **built-in string functions** to manipulate text.

### **Common String Functions:**

1. **`split()`** → Splits a string into a list.

   ```
   name = "Abhishek Veeramalla"
   first_name = name.split()[0]
   print(first_name)  # Output: Abhishek
   ```

2. **`upper()`** → Converts string to uppercase.

   ```
   text = "hello"
   print(text.upper())  # Output: HELLO
   ```

3. **`lower()`** → Converts string to lowercase.

   ```
   text = "HELLO"
   print(text.lower())  # Output: hello
   ```

4. **`replace()`** → Replaces a substring.

   ```
   text = "Hello World"
   print(text.replace("World", "Python"))  # Output: Hello Python
   ```

5. **`strip()`** → Removes whitespace from both ends.

   ```
   text = "  hello  "
   print(text.strip())  # Output: "hello"
   ```

6. **`find()`** → Finds the index of a substring.

   ```
   text = "Hello Python"
   print(text.find("Python"))  # Output: 6
   ```

7. **String Concatenation** → Joining strings together.

   ```
   str1 = "Hello"
   str2 = "World"
   result = str1 + " " + str2
   print(result)  # Output: Hello World
   ```

------

## **5. Numeric Data Types and Functions**

### **Integer (`int`) and Float (`float`)**

- Integers are whole numbers: `10`, `20`
- Floats contain decimals: `3.14`, `5.0`

### **Common Numeric Functions:**

1. **`abs()`** → Returns absolute value.

   ```
   num = -10
   print(abs(num))  # Output: 10
   ```

2. **`round()`** → Rounds a float to a given number of decimal places.

   ```
   pi = 3.141592
   print(round(pi, 2))  # Output: 3.14
   ```

------

## **6. Regular Expressions in Python**

- **Regular expressions (regex)** help search for patterns in strings.
- **Useful for DevOps Engineers**: Parsing logs, extracting information from text.

### **Basic Example: Checking for a word in a sentence**

```
import re

text = "The quick brown fox jumps over the lazy dog"
pattern = "quick"

if re.search(pattern, text):
    print("Pattern found!")
else:
    print("Pattern not found!")
```

**Output:** `Pattern found!`

### **Use Case in DevOps: Extracting AWS ARN Username**

AWS **ARN (Amazon Resource Name)** format:

```
arn:aws:iam::123456789:user/abhishek
```

Extract the username:

```
arn = "arn:aws:iam::123456789:user/abhishek"
username = arn.split("/")[-1]  # Splits by '/' and takes the last part
print(username)  # Output: abhishek
```