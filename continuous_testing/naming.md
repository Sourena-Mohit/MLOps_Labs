# Pytest Overview

Pytest is a popular testing framework in Python used for writing and running tests. It’s known for its simplicity, scalability, and compatibility with existing Python testing frameworks like `unittest`.

For pytest to automatically discover and execute your test files and functions, you need to follow specific naming conventions.

---

## Naming Conventions in Pytest

### 1. **Test File Naming**
Test files must be named in a way that pytest can recognize them as test files.

**Rules:**
- Files should start with `test_` or end with `_test.py`.

**Example test files:**
```python
test_example.py
example_test.py
```

### 2. **Test Function Naming**

Inside the test files, functions that contain test cases must follow specific naming rules to ensure pytest recognizes and executes them.

#### **Rules:**
- Functions should start with `test_`.

#### **Example Test Functions:**
```python
def test_addition():
    assert 1 + 1 == 2

def test_subtraction():
    assert 2 - 1 == 1
```

### 3. **Test Class Naming (Optional)**

If you use classes to organize tests, the class names should start with `Test`. This approach is optional but helps in organizing related test cases together.

#### **Rules:**
- The class should not have an `__init__` method (pytest doesn’t recognize classes with `__init__` as test cases).
- Inside the class, functions should still follow the `test_` naming convention.

#### **Example:**
```python
class TestMathOperations:
    def test_addition(self):
        assert 1 + 1 == 2

    def test_subtraction(self):
        assert 2 - 1 == 1
```

### 4. **Directory Naming**

If you organize your tests into directories, those directories must follow specific naming patterns for pytest to discover them correctly.

#### **Rules:**
- Test directories should have names like `tests` or start with `test_`.
- Use an `__init__.py` file in the directory if you want to treat it as a package (optional for pytest, but useful for certain use cases).

#### **Example Directory Structure:**
my_project/
├── src/
│   └── main.py
└── tests/
    ├── __init__.py
    ├── test_main.py
    └── test_utils.py


## Summary of Naming Rules

| **Component**       | **Naming Rule**                          | **Example**                     |
|----------------------|------------------------------------------|----------------------------------|
| **Test Files**       | Start with `test_` or end with `_test.py`| `test_example.py`, `example_test.py` |
| **Test Functions**   | Start with `test_`                      | `def test_example():`           |
| **Test Classes**     | Start with `Test`                       | `class TestExample:`            |
| **Test Directories** | Start with `test_` or named `tests`     | `tests/`, `test_suite/`         |


## How Pytest Discovers Tests

### **Pytest Search Path**
- By default, pytest searches for tests in the current directory and its subdirectories.
- It identifies test files, classes, and functions based on the naming conventions.

#### **Example Command:**
```bash
pytest
```
Explicit File/Directory
You can specify a particular file or directory to run tests instead of running all tests.
Example Commands:
```bash
pytest tests/             # Runs all tests in the 'tests' directory
pytest tests/test_example.py  # Runs all tests in 'test_example.py'
```
Discovered Tests
Pytest automatically detects and executes files, classes, and functions that follow the naming conventions:
Files starting with test_ or ending with _test.py
Classes starting with Test
Functions starting with test_

## Running Pytest

### **1. Install pytest (if not already installed):**
Use `pip` to install pytest in your environment:
```bash
pip install pytest
```

2. Run Tests:
Run all tests in the current directory and its subdirectories:
```bash
pytest
```
3. Run Tests with More Output:
Use the -v flag for more detailed output, showing each test and its result:
```bash
pytest -v
```
This is especially helpful for debugging and tracking test results.





