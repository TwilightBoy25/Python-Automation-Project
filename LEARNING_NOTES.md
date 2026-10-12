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

## Learning Note 009 — Comparison Operators and Boolean Values

**Objective:** Understand how Python evaluates comparisons.

**Concepts:**
- Comparison operators compare values.
- `>` greater than; `<` less than.
- `>=` greater than or equal to; `<=` less than or equal to.
- `==` equal to; `!=` not equal to.
- Comparisons produce Boolean values: `True` or `False`.
- `=` assigns a value, while `==` checks equality.
- `python3` opens the interactive Python interpreter.
- `exit()` returns to the Linux shell.

**Practice:**
```python
85 > 80  # True
85 < 80  # False
```
## Learning Note 010 — Python Conditional Statements

**Objective:** Understand how Python makes decisions using `if` statements.

**Concepts:**
- `if` evaluates a condition.
- When the condition is `True`, Python executes the indented block.
- When the condition is `False`, Python skips that block.
- A colon (`:`) begins the conditional block.
- Indentation defines which statements belong to the block.
- `>` and `>=` differ at the threshold boundary.

**Example:**
```python
if cpu_usage > 80:
    print("WARNING")
```

**Key takeaway:** Conditional statements allow monitoring scripts to react to system metrics rather than only display them.

**Current project status:** CPU usage is simulated, not collected from the operating system.
**Automation connection:** Comparison operators will allow our monitoring script to determine when CPU utilization exceeds a warning threshold.

## Learning Note 011 — Testing Conditional Logic

**Objective:** Verify how Python executes an `if` statement.

**Concepts:**
- `cpu_usage` stores the simulated CPU utilization value.
- `80` is the warning threshold.
- `85 > 80` evaluates to `True`.
- `75 > 80` evaluates to `False`.
- Python executes an `if` block only when its condition is true.
- Statements outside the `if` block execute normally.

**Expected output with cpu_usage = 85:**
```text
Linux Server Health Monitor
RHEL-10
85
WARNING
```

**Key takeaway:** Testing code verifies that the program behaves as predicted. Later, we will test values above, below, and exactly at the threshold.

## Learning Note 012 — Python if/else Statements

**Objective:** Understand how Python handles true and false conditions.

**Concepts:**
- `if` evaluates a condition.
- When the condition is True, Python executes the `if` block.
- When the condition is False, Python executes the `else` block.
- `else` does not require a condition.
- Indentation defines which statements belong to each block.

**Example:**
```python
if cpu_usage > 80:
    print("WARNING")
else:
    print("HEALTHY")
```

**Key takeaway:** if/else statements allow our Linux monitoring script to choose between two outcomes.

**Note:** CPU utilization is simulated for now.

## Learning Note 013 — Verifying if/else Control Flow

**Objective:** Verify that Python executes the correct conditional branch.

**Concepts:**
- Control flow determines which instructions execute.
- `if/else` provides two mutually exclusive execution paths.
- A condition evaluates to a Boolean value (`True` or `False`).
- If the condition is `True`, Python executes the `if` block.
- If the condition is `False`, Python executes the `else` block.

**Test case:**
- `cpu_usage = 85`
- Condition: `85 > 80`
- Expected result: `WARNING`

**Key takeaway:** Running a script and comparing actual output to expected output is an essential software testing practice.

## Learning Note 014 — Testing Both Conditional Branches

**Objective:** Verify the False branch of an if/else statement.

**Concepts:**
- An if/else statement has two possible execution paths.
- Testing both branches helps verify program behavior.
- When cpu_usage = 85, the condition 85 > 80 is True and prints WARNING.
- When cpu_usage = 60, the condition 60 > 80 is False and prints HEALTHY.
- Change one variable at a time when testing to isolate the cause of different results.

**Test cases:**
- CPU 85 → WARNING (verified)
- CPU 60 → HEALTHY (pending verification)

**Key takeaway:** Testing both True and False outcomes is a basic software engineering practice.

**Note:** CPU utilization is simulated, not collected from the actual Linux system.

## Learning Note 015 — Boundary Testing

**Objective:** Understand why software engineers test values at the exact threshold.

**Concepts:**
- Boundary testing checks behavior at or near a condition's threshold.
- The `>` operator means strictly greater than.
- The `>=` operator means greater than or equal to.
- Testing values below, at, and above a threshold helps detect logic errors.

**Current test cases:**
- cpu_usage = 60 → HEALTHY (verified)
- cpu_usage = 85 → WARNING (verified)
- cpu_usage = 80 → Pending

**Key takeaway:** Boundary testing helps verify that monitoring and alerting logic behaves correctly at threshold values.

**Note:** CPU usage is simulated; real system metrics will be introduced later.

## Learning Note 016 — Configurable Thresholds

**Objective:** Learn to store monitoring thresholds in variables instead of hardcoding them inside conditions.

**Concepts:**
- A hardcoded value is written directly into program logic.
- Variables make configuration easier to change and understand.
- `cpu_threshold = 80` stores the warning threshold.
- `cpu_usage > cpu_threshold` compares two integer values.
- Separating configuration from decision-making logic improves maintainability.

**Example:**
```python
cpu_usage = 80
cpu_threshold = 80

if cpu_usage > cpu_threshold:
    print("WARNING")
else:
    print("HEALTHY")
```

**Key takeaway:** Configurable thresholds make automation scripts easier to maintain and adapt.

**Current project status:** CPU values remain simulated; real system metrics are a future milestone.

## Learning Note 017 — Verifying Configurable Thresholds

**Objective:** Verify that replacing a hardcoded threshold with a variable preserves program behavior.

**Concepts:**
- Configuration values can be stored in variables.
- `cpu_threshold = 80` defines the warning threshold.
- `cpu_usage > cpu_threshold` compares two integer values.
- Changing how code is structured should not unintentionally change its behavior.
- Testing after code changes helps detect regressions.

**Test case:**
- CPU usage: 80
- CPU threshold: 80
- Comparison: 80 > 80 → False
- Expected result: HEALTHY

**Key takeaway:** Verify that code improvements preserve the expected behavior before adding more features.

**Project status:** CPU utilization remains simulated.

## Learning Note 018 — Testing Configuration Changes

**Objective:** Verify that changing a configurable threshold changes the monitoring decision.

**Concepts:**
- Configuration values control how a program behaves.
- `cpu_usage` represents simulated CPU utilization.
- `cpu_threshold` defines the warning threshold.
- Changing a threshold does not require rewriting the conditional logic.
- Testing one change at a time makes troubleshooting easier.

**Test case:**
```python
cpu_usage = 80
cpu_threshold = 70
```

**Expected comparison:** `80 > 70` → `True`

**Expected status:** `WARNING`

**Key takeaway:** Separating configuration from logic allows a monitoring script to adapt to changing operational requirements.

**Project status:** CPU values remain simulated; real Linux metrics will be introduced later.

## Learning Note 019 — Introduction to the Linux /proc Filesystem

**Objective:** Discover how Linux exposes real system statistics.

**Concepts:**
- `/proc` is a virtual filesystem that exposes kernel and process information.
- `/proc/stat` provides CPU activity counters.
- `/proc/meminfo` provides memory statistics.
- `/proc/uptime` provides system uptime.
- The kernel generates these values dynamically.
- CPU counters in `/proc/stat` are cumulative time measurements, not CPU usage percentages.

**Command:**
```bash
head -n 5 /proc/stat
```

**Command breakdown:**
- `head`: Displays the beginning of a file.
- `-n 5`: Displays five lines.
- `/proc/stat`: Source of kernel CPU statistics.

**Key takeaway:** Linux system-monitoring programs can obtain real measurements from kernel-provided interfaces instead of relying on simulated values.

**Project status:** Exploring real system data; monitor.py has not yet been modified to read it.
