# Ch-01 | Introduction to Python | Shell Scripting vs Python | Install and Run

## **1. Why DevOps Engineers Use Python**

- Python is widely used by DevOps engineers due to its versatility.
- It is preferred for automation, API interactions, and complex scripting tasks.
- Shell scripting is useful for system administration tasks but has limitations.

## **2. Shell Scripting vs Python**

### **Shell Scripting:**

- Primarily used for Linux system interaction.
- Useful for simple automation tasks like:
  - Creating files and directories.
  - Fetching system information (CPU usage, memory, disk space).
  - Managing processes and services.
- Typically executed via `.sh` files.
- Commands run sequentially when executed.

### **Python Scripting:**

- Works on both **Linux and Windows** (unlike shell scripting).
- Can handle **complex logic**, **API interactions**, and **data processing**.
- Preferred for:
  - Working with **APIs** (e.g., fetching GitHub issues).
  - **Data manipulation** (e.g., handling JSON, CSV).
  - **Cross-platform automation** (Windows, Linux, Mac).
  - **Advanced scripting** (e.g., integrating with AWS Lambda).

### **Key Differences:**

| Feature         | Shell Scripting             | Python Scripting                     |
| --------------- | --------------------------- | ------------------------------------ |
| Platform        | Linux only                  | Cross-platform (Linux, Windows, Mac) |
| Ease of Use     | Simple tasks                | Suitable for complex automation      |
| API Interaction | Limited                     | Strong API support (requests module) |
| Data Handling   | Basic (JQ for JSON parsing) | Advanced (pandas, JSON module)       |
| Error Handling  | Limited                     | Robust error handling (try-except)   |

## **3. Installing Python & Running First Program**

### **Option 1: Using GitHub Codespaces**

- Provides a pre-configured environment for Python.
- Offers **60 hours of free usage per month**.
- No need to install Python locally.

**Steps:**

1. Open GitHub repository.

2. Click on **Codespaces** and launch a new instance.

3. Run:

   ```
   python --version
   ```

   to check installation.

4. Navigate to the project folder and execute:

   ```
   python filename.py
   ```

### **Option 2: Installing Python Locally**

#### **Windows:**

1. Download Python from [official site](https://www.python.org/downloads/).

2. Choose **64-bit** version (for most modern PCs).

3. Install Python and ensure **“Add Python to PATH”** is checked.

4. Verify installation:

   ```
   python --version
   ```

#### **Mac:**

- Use Homebrew:

  ```
    brew install python
  ```

- Check installation:

  ```
  python3 --version
  ```

#### **Linux:**

- Install using package manager:

  ```
  sudo apt install python3  # Ubuntu/Debian
  sudo yum install python3  # CentOS/RHEL
  ```

## **4. Running a Python Script**

- Create a simple Python script

  ```
  hello.py
  ```

  ```
  print("Hello, Python!")
  ```

- Run it using:

  ```
  python hello.py
  ```

------

### **Assignment:**

1. Set up Python using **GitHub Codespaces** or install it locally.
2. Run a simple Python script.
3. Review **Day-1** materials in the provided GitHub repository.