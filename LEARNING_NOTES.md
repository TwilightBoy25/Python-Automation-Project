## Learning Note 001 — Linux Project Directories

**Objective:** Create and navigate a project directory in Linux.

**Commands:**
- `pwd` — Print working directory.
- `mkdir` — Create a directory.
- `mkdir -p` — Create parent directories as needed.
- `cd` — Change directory.
- `~` — Current user's home directory.

**Key takeaway:** Linux projects can be organized into directories, making scripts and related files easier to manage.

**Verification:** Run `pwd` to confirm the current directory.

## Learning Note 002 — Python Interpreter

**Objective:** Verify Python 3 is available on RHEL 10.

**Command:** `python3 --version`

**Concepts:**
- Python is an interpreted programming language.
- The Python interpreter executes Python code.
- `python3` invokes the Python 3 interpreter.
- `--version` displays the interpreter version.

**Verification:** Run `python3 --version` and record the output.

## Learning Note 003 — Creating Python Scripts with Vim

**Objective:** Create and save a Python source file using Vim.

**Command:** `vim monitor.py`

**Concepts:**
- `.py` identifies a Python source file.
- Vim Normal Mode is used for navigation and commands.
- Press `i` to enter Insert Mode.
- Press `Esc` to return to Normal Mode.
- `:wq` saves the file and quits Vim.
- `print()` is a built-in Python function used to display output.
- Text enclosed in quotes is a string.

**Practice:** Create `monitor.py` and add `print("Linux Server Health Monitor")`.

## Learning Note 004 — Executing Python Scripts in Linux

**Objective:** Execute a Python script using the Python 3 interpreter.

**Command:** `python3 monitor.py`

**Concepts:**
- `python3` invokes the Python interpreter.
- `monitor.py` is the source file passed to the interpreter.
- Python executes the instructions contained in the file.
- `print()` displays text in the terminal.
- Running `python3 monitor.py` does not require executable permissions on the script.

**Key takeaway:** The Python interpreter allows us to execute scripts directly from the Linux command line.

**Expected output:** Linux Server Health Monitor

## Learning Note 005 — Python Variables and Strings

**Objective:** Understand how Python stores and references values.

**Concepts:**
- A variable is a name that refers to a value.
- The `=` operator assigns a value to a variable.
- A string is text enclosed in quotation marks.
- `print()` displays a value in the terminal.
- Variables allow programs to reuse information without repeating literal values.

**Example:**
```python
server_name = "RHEL-10"
print(server_name)
```

**Key takeaway:** Variables will allow our monitoring script to store and process system information.

## Learning Note 006 — Python Execution Order & Output

**Objective:** Understand how Python executes statements and prints variable values.

**Concepts:**
- Python normally executes statements sequentially, from top to bottom.
- Assigning a variable does not automatically display its value.
- `print()` displays the value of an expression.
- Each `print()` call ends with a newline by default.
- `print(server_name)` prints the variable's value, not its name.

**Example:**
```python
server_name = "RHEL-10"
print("Linux Server Health Monitor")
print(server_name)
```

**Expected output:**
```text
Linux Server Health Monitor
RHEL-10
```

**Key takeaway:** Predicting program output before execution helps develop debugging and code-reading skills.

## Learning Note 007 — Python Data Types: Integers

**Objective:** Understand integer variables and their role in automation.

**Concepts:**
- `int` represents whole numbers.
- `str` represents text enclosed in quotation marks.
- `float` represents floating-point numbers.
- `85` is an integer, while `"85"` is a string.
- Numerical values can be used in calculations and threshold comparisons.

**Example:**
```python
server_name = "RHEL-10"
cpu_usage = 85

print("Linux Server Health Monitor")
print(server_name)
print(cpu_usage)
```

**Key takeaway:** Correct data types are important when writing automation that analyzes system metrics.

**Note:** The CPU value is simulated for now, not a real measurement.

## Learning Note 008 — Data Types and Numerical Comparisons

**Objective:** Understand why numerical data types matter in Python automation.

**Concepts:**
- Integers (`int`) represent whole numbers.
- Strings (`str`) represent text.
- `85` is an integer; `"85"` is a string.
- Numerical comparisons such as `85 > 80` evaluate to a Boolean (`True` or `False`).
- Comparing a string directly with an integer using `>` raises a TypeError in Python 3.
- `int("72")` converts a valid numeric string to an integer.

**Key takeaway:** The data type, not the specific numerical value, determines whether a value can be used directly in numerical comparisons.
