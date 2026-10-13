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

## Learning Note 020 — Exploring Linux Memory Statistics

**Objective:** Learn how Linux exposes real memory statistics through /proc/meminfo.

**Command:**
```bash
head -n 5 /proc/meminfo
```

**Concepts:**
- /proc/meminfo is a kernel-provided interface for memory statistics.
- MemTotal: Total usable physical memory.
- MemFree: Memory currently unused.
- MemAvailable: Estimated memory available for applications without swapping.
- Buffers: Memory used for certain kernel buffers.
- Cached: Memory used for the page cache.
- Linux can reclaim some cached memory when applications need it.

**Engineering takeaway:** MemAvailable is often a better indicator of usable memory than MemFree alone.

**Project status:** Exploring real Linux system metrics. No changes to monitor.py yet.

## Learning Note 021 — Inspecting Disk Utilization

**Objective:** Learn how to inspect filesystem storage usage in Linux.

**Command:**
```bash
df -h /
```

**Concepts:**
- `df` reports filesystem space usage.
- `-h` displays human-readable storage units.
- `/` selects the filesystem containing the root directory.
- `Size` represents total filesystem capacity.
- `Used` represents occupied filesystem space.
- `Avail` represents space available to unprivileged users.
- `Use%` reports filesystem utilization as a percentage.
- `Mounted on` identifies the mount point.

**Engineering takeaway:** Disk utilization is an important system-health metric because full filesystems can prevent applications from writing logs, creating files, or completing operations.

**Project status:** Exploring real CPU, memory, and disk statistics before integrating them into Python.

## Learning Note 022 — Introduction to Python's os Module

**Objective:** Learn how Python can retrieve information from the Linux operating system.

**Command:**
```bash
python3 -c "import os; print(os.getloadavg())"
```

**Concepts:**
- A Python module contains reusable functions and other definitions.
- `import os` makes operating-system functionality available to Python.
- `python3 -c` executes Python code directly from the terminal.
- `os.getloadavg()` returns the system's 1-minute, 5-minute, and 15-minute load averages.
- The three results are returned as a tuple.
- Load average is not the same as CPU utilization percentage.

**Engineering takeaway:** Python can interact with operating-system interfaces to collect real monitoring information.

**Project status:** Beginning Python-based system metric collection. monitor.py remains unchanged.

## Learning Note 023 — Tuple Indexing in Python

**Objective:** Learn to retrieve individual values from a tuple.

**Command:**
```bash
python3 -c "import os; print(os.getloadavg()[0])"
```

**Concepts:**
- A tuple is an ordered collection of values.
- Python uses zero-based indexing.
- Index [0] accesses the first element.
- Index [1] accesses the second element.
- Index [2] accesses the third element.
- os.getloadavg() returns a tuple containing the 1-minute, 5-minute, and 15-minute system load averages.

**Examples:**
```python
os.getloadavg()[0]  # 1-minute load average
os.getloadavg()[1]  # 5-minute load average
os.getloadavg()[2]  # 15-minute load average
```

**Engineering takeaway:** Indexing allows monitoring scripts to extract specific measurements from collections of system data.

**Project status:** Practicing metric extraction before integrating real measurements into monitor.py.

## Learning Note 024 — Storing System Metrics in Variables

**Objective:** Learn to assign real Linux system measurements to Python variables.

**Command:**
```bash
python3 -c "import os; load_average = os.getloadavg()[0]; print(load_average)"
```

**Concepts:**
- The assignment operator (`=`) stores a value in a variable.
- `os.getloadavg()` retrieves three system load averages.
- `[0]` selects the 1-minute load average.
- `load_average` stores the selected measurement.
- `print(load_average)` displays the stored value.
- Variables allow measurements to be reused in calculations and conditional statements.

**Example:**
```python
import os

load_average = os.getloadavg()[0]
print(load_average)
```

**Engineering takeaway:** Collecting a system metric and storing it in a variable allows automation scripts to evaluate, process, and report that measurement.

**Important:** System load average is not equivalent to CPU utilization percentage.

**Project status:** Practicing real metric collection before integrating it into monitor.py.

## Learning Note 025 — Integrating OS Metrics into Python

**Objective:** Add real Linux system data collection to monitor.py.

**New code:**
```python
import os

load_average = os.getloadavg()[0]
```

**Concepts:**
- Imports are conventionally placed at the beginning of Python files.
- `os.getloadavg()[0]` retrieves the 1-minute system load average.
- Assigning the result to `load_average` stores a snapshot of the measurement.
- Variables do not automatically update when the operating system changes.
- Python executes statements in order.
- `cpu_usage` remains a simulated percentage and must not be confused with load average.

**Engineering takeaway:** Integrating OS functions into a Python script allows us to begin collecting real infrastructure metrics.

**Checkpoint:** Add the import and assignment, save monitor.py, and predict whether the existing output will change. Do not execute yet.

## Learning Note 026 — Regression Testing After Integration

**Objective:** Verify that adding real system metric collection does not break existing monitoring logic.

**Command:**
```bash
python3 monitor.py
```

**Expected output:**
```text
Linux Server Health Monitor
RHEL-10
80
WARNING
```

**Concepts:**
- Regression testing checks whether existing functionality still works after code changes.
- `import os` does not print output by itself.
- `load_average = os.getloadavg()[0]` retrieves and stores a measurement without displaying it.
- Existing print statements determine what appears in the terminal.
- Testing changes incrementally helps isolate bugs.

**Engineering takeaway:** After introducing a new dependency or feature, verify that previously working functionality remains intact.

**Project status:** Real system load collection has been added; execution verification is pending.

## Learning Note 027 — Source Code Inspection

**Objective:** Verify the current source code before making further changes.

**Command:**
```bash
cat monitor.py
```

**Concepts:**
- `cat` displays the contents of a file.
- Source code inspection helps identify unexpected configuration values.
- Program output should be evaluated against the code that actually executed.
- Regression testing checks both successful execution and expected behavior.
- Troubleshooting should begin with evidence rather than assumptions.

**Observation:**
- Checkpoint 26 displayed CPU usage of 85.
- Our previous documented value was 80.
- We need to inspect monitor.py to identify its current configuration.

**Engineering takeaway:** Verify the actual system state before modifying code or troubleshooting unexpected behavior.

**Project status:** Confirming the script's current configuration before adding a new feature.

## Learning Note 028 — Displaying Real System Metrics

**Objective:** Display the real Linux load average collected by Python.

**New code:**
```python
print(load_average)
```

**Concepts:**
- `os.getloadavg()[0]` retrieves the 1-minute load average.
- `load_average` stores a snapshot of that measurement.
- `print(load_average)` displays the stored value.
- `cpu_usage` remains a simulated CPU percentage.
- Load average is not equivalent to CPU utilization percentage.
- The existing warning condition still evaluates `cpu_usage > cpu_threshold`.

**Expected output structure:**
```text
Linux Server Health Monitor
RHEL-10
85
<real load average>
WARNING
```

**Engineering takeaway:** Monitoring software separates metric collection, data presentation, and alert evaluation.

**Project status:** Displaying our first real Linux system measurement inside monitor.py.

## Learning Note 029 — Labeled Monitoring Output

**Objective:** Improve the readability of Linux monitoring output using Python's print() function.

**New code:**
```python
print("1-Minute Load Average:", load_average)
```

**Concepts:**
- `print()` accepts multiple arguments separated by commas.
- A string can be used as a label to describe a measurement.
- Python separates print arguments with a space by default.
- `load_average` contains a real Linux system load measurement.
- Labeled output makes monitoring results easier to interpret and troubleshoot.

**Example output:**
```text
1-Minute Load Average: 0.24
```

**Engineering takeaway:** Clear labels improve the readability of operational output and help engineers identify measurements without guessing.

**Project status:** Improving the presentation of real Linux system metrics.

## Learning Note 030 — Displaying Multiple Arguments and Units

**Objective:** Make simulated CPU output easier to interpret by adding a label and unit.

**New code:**
```python
print("Simulated CPU Usage:", cpu_usage, "%")
```

**Concepts:**
- Python's print() function accepts multiple arguments.
- Commas separate arguments in the function call.
- By default, print() inserts spaces between arguments.
- Strings can describe metrics and their units.
- Clearly identifying simulated measurements prevents confusion with real system data.

**Expected output:**
```text
Simulated CPU Usage: 85 %
```

**Engineering takeaway:** Monitoring output should identify each metric, its unit, and whether the value is simulated or collected from the operating system.

**Project status:** Improving the clarity of simulated and real monitoring data.

## Learning Note 031 — Introduction to Python f-Strings

**Objective:** Use formatted string literals to display variables inside readable monitoring output.

**New code:**
```python
print(f"Simulated CPU Usage: {cpu_usage}%")
```

**Concepts:**
- An f-string is a formatted string literal.
- Prefixing a string with `f` enables interpolation.
- Curly braces `{}` allow Python expressions or variables to be evaluated inside a string.
- Unlike multiple print() arguments, f-strings let us control spacing precisely.
- F-strings are useful for monitoring messages, logs, and automation output.

**Expected output:**
```text
Simulated CPU Usage: 85%
```

**Engineering takeaway:** F-strings make it easier to construct clear, consistently formatted operational messages.

**Project status:** Introducing formatted strings to improve monitoring output.

## Learning Note 032 — Formatting Floating-Point Numbers

**Objective:** Format Linux load-average measurements to two decimal places using Python f-strings.

**New code:**
```python
print(f"1-Minute Load Average: {load_average:.2f}")
```

**Concepts:**
- F-strings support formatting specifications inside curly braces.
- `:` introduces the formatting specification.
- `.2f` displays a number with two digits after the decimal point.
- Formatting changes the displayed representation, not the original variable value.
- Consistent numerical formatting improves the readability of monitoring output.

**Example:**
```text
Original value: 0.30859375
Formatted output: 0.31
```

**Engineering takeaway:** Monitoring tools should display measurements with useful precision while retaining the original data for calculations.

**Project status:** Improving the presentation of real Linux load-average measurements.

## Learning Note 033 — Comparison Operators and Threshold Boundaries

**Objective:** Understand how Python evaluates conditions at an exact monitoring threshold.

**Example:**
```python
cpu_usage = 70
cpu_threshold = 70

if cpu_usage > cpu_threshold:
    print("WARNING")
else:
    print("HEALTHY")
```

**Concepts:**
- `>` means strictly greater than.
- `>=` means greater than or equal to.
- An `if` statement evaluates a Boolean condition.
- The `else` branch runs when the `if` condition is False.
- Boundary testing verifies behavior when a metric equals its configured threshold.

**Engineering takeaway:** Alerting logic must clearly define whether a threshold is inclusive or exclusive.

**Project status:** Reviewing threshold boundaries before introducing real Linux health checks.

## Learning Note 034 — Inclusive vs. Exclusive Thresholds

**Objective:** Understand how inclusive thresholds affect monitoring alerts.

**Comparison operators:**
```python
cpu_usage > cpu_threshold
cpu_usage >= cpu_threshold
```

**Concepts:**
- `>` means strictly greater than.
- `>=` means greater than or equal to.
- An exclusive threshold does not trigger at the exact threshold value.
- An inclusive threshold triggers when the measured value equals or exceeds the threshold.
- Monitoring policies determine which comparison operator is appropriate.

**Example:**
```python
cpu_usage = 70
cpu_threshold = 70

if cpu_usage >= cpu_threshold:
    print("WARNING")
else:
    print("HEALTHY")
```

**Engineering takeaway:** Choose comparison operators based on the intended alerting policy, especially at threshold boundaries.

**Project status:** Practicing inclusive threshold logic before introducing real system alerts.

## Learning Note 035 — Implementing Inclusive CPU Thresholds

**Objective:** Update the simulated CPU alert condition to use an inclusive threshold.

**Previous code:**
```python
if cpu_usage > cpu_threshold:
```

**Updated code:**
```python
if cpu_usage >= cpu_threshold:
```

**Concepts:**
- `>` triggers only when the measured value exceeds the threshold.
- `>=` triggers when the measured value equals or exceeds the threshold.
- With cpu_usage = 85 and cpu_threshold = 70, both operators evaluate to True.
- Changing a comparison operator may affect boundary behavior without changing the current output.
- Testing after a small code change helps verify existing functionality.

**Engineering takeaway:** Monitoring thresholds should match the exact alerting policy, including whether the boundary is inclusive.

**Project status:** Implementing inclusive threshold logic in monitor.py.

## Learning Note 036 — Boundary Testing an Inclusive Threshold

**Objective:** Verify that an inclusive CPU threshold triggers at the exact boundary.

**Test configuration:**
```python
cpu_usage = 70
cpu_threshold = 70
```

**Condition:**
```python
if cpu_usage >= cpu_threshold:
    print("WARNING")
else:
    print("HEALTHY")
```

**Expected status:** WARNING

**Concepts:**
- Boundary testing checks behavior at the exact threshold.
- `>=` evaluates to True when both operands are equal.
- Changing one variable at a time makes test results easier to interpret.
- The load average remains a real system measurement, separate from simulated CPU usage.

**Engineering takeaway:** Monitoring systems need tests at threshold boundaries to confirm that alerts follow the intended policy.

**Project status:** Testing inclusive alert behavior with equal simulated CPU usage and threshold values.

## Learning Note 037 — Testing Below an Inclusive Threshold

**Objective:** Verify that simulated CPU usage below the configured threshold produces a healthy status.

**Test configuration:**
```python
cpu_usage = 69
cpu_threshold = 70
```

**Condition:**
```python
if cpu_usage >= cpu_threshold:
    print("WARNING")
else:
    print("HEALTHY")
```

**Expected status:** HEALTHY

**Concepts:**
- `>=` evaluates to False when the left operand is smaller than the right operand.
- The `else` branch executes when the `if` condition is False.
- Boundary testing should cover values below, equal to, and above a threshold.
- Changing one variable at a time helps isolate the behavior being tested.
- Real Linux load average remains independent of the simulated CPU warning.

**Engineering takeaway:** A monitoring system must distinguish healthy measurements from values that meet or exceed an alert threshold.

**Project status:** Completing simulated CPU threshold boundary tests before adding real metric-based alerting.

