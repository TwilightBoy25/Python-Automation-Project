# Python Automation Project

> **Learning Python through Linux System Administration and IT Operations**

## Project Overview

**Objective:** Build a Python automation tool that monitors Linux system health, detects potential issues, and generates diagnostic reports.

This project focuses on developing practical Python programming skills for Linux System Administration, DevOps, Site Reliability Engineering (SRE), and AI Infrastructure Operations.

**Development approach:** Learn the concepts, write the code independently, test each component, and document the results.

---

## 1. Understanding Python Automation

Python automation involves writing programs that perform repetitive tasks with minimal manual intervention.

### Common IT Automation Tasks

- Monitor CPU, memory, and disk usage.
- Check system uptime and availability.
- Analyze logs for errors.
- Identify abnormal system conditions.
- Generate diagnostic reports.
- Automate repetitive administrative tasks.

### Linux Commands

```bash
uptime       # Display system uptime and load averages
free -h      # Display memory usage in human-readable format
df -h        # Display filesystem disk usage
```

**Key takeaway:** Automation follows a process: collect information, evaluate conditions, and produce useful results.

---

## 2. Project Workflow

```text
Start Python Program
        |
        v
Collect System Information
        |
        v
Analyze Resource Usage
        |
        v
Compare Against Thresholds
        |
        v
Identify Potential Issues
        |
        v
Generate Diagnostic Report
        |
        v
Log Results
```

---

## 3. Python Fundamentals

### 3.1 Variables and Data Types

Variables store values that a program can reference.

```python
server_name = "RHEL-Server"  # String
cpu_usage = 45              # Integer
memory_usage = 62.5         # Float
server_online = True        # Boolean
```

**Concepts to understand:**
- Variables and assignment
- Strings, integers, floats, and booleans
- Accessing and updating values

### 3.2 Conditional Statements

Conditional statements allow programs to make decisions.

```python
cpu_usage = 85

if cpu_usage > 80:
    print("WARNING: High CPU usage")
else:
    print("CPU usage is normal")
```

**Key takeaway:** Conditional logic enables an automation script to respond to different system conditions.

### 3.3 Functions

Functions organize reusable blocks of code.

```python
def check_server():
    print("Checking server health")

check_server()
```

**Concepts to understand:**
- Defining functions with `def`
- Calling functions
- Parameters and arguments
- Return values
- Reusing code

### 3.4 Python Modules

Modules provide additional functionality that programs can import.

| Module | Purpose |
|---|---|
| `os` | Interact with operating-system features |
| `subprocess` | Execute external system commands |
| `datetime` | Work with dates and timestamps |
| `logging` | Record program events |
| `pathlib` | Work with filesystem paths |
| `shutil` | Access filesystem and disk-usage utilities |

---

## 4. Development Roadmap

### Phase 1: Python Fundamentals

- [ ] Practice variables and data types.
- [ ] Understand conditional statements.
- [ ] Practice loops.
- [ ] Learn functions and return values.
- [ ] Understand modules and imports.

**Goal:** Write simple Python programs independently.

### Phase 2: Linux System Integration

- [ ] Learn how Python interacts with Linux.
- [ ] Retrieve system information.
- [ ] Collect CPU and memory statistics.
- [ ] Check disk utilization.
- [ ] Handle command execution errors.

**Goal:** Collect useful system information from a Linux environment.

### Phase 3: Monitoring and Alerts

- [ ] Define resource utilization thresholds.
- [ ] Compare system metrics against thresholds.
- [ ] Identify abnormal conditions.
- [ ] Generate warning messages.
- [ ] Handle unexpected values and errors.

**Goal:** Turn system metrics into actionable diagnostic information.

### Phase 4: Logging and Reporting

- [ ] Learn Python's `logging` module.
- [ ] Add timestamps to events.
- [ ] Record monitoring results.
- [ ] Generate readable diagnostic reports.
- [ ] Save reports to files.

**Goal:** Maintain useful records for troubleshooting.

### Phase 5: Testing and Documentation

- [ ] Test normal operating conditions.
- [ ] Simulate high resource utilization.
- [ ] Test error handling.
- [ ] Refactor repetitive code.
- [ ] Document installation and usage.
- [ ] Include example output.

**Goal:** Build a reliable and maintainable automation tool.

---

## 5. Engineering Principles

1. **Understand before implementing:** Explain the purpose of each line of code.
2. **Build incrementally:** Develop and test one component at a time.
3. **Troubleshoot systematically:** Investigate errors before applying fixes.
4. **Prioritize readability:** Write understandable and maintainable code.
5. **Document decisions:** Record lessons, challenges, and solutions.
6. **Avoid unnecessary complexity:** Start simple and improve gradually.

---

## 6. Career Applications

| Engineering Field | Relevant Skills |
|---|---|
| Linux System Administration | Monitoring and troubleshooting |
| DevOps | Scripting and automation |
| Site Reliability Engineering | Observability and incident detection |
| AI Operations | Production infrastructure monitoring |
| AI Infrastructure Security | Operational visibility and anomaly detection |

---

## 7. Learning Journal

### Session 1: Project Planning

**Topics:**
- Understanding Python automation
- Identifying IT operations use cases
- Designing the project workflow
- Establishing development milestones

**Key lesson:**

An automation program can collect information, analyze it, make decisions, and produce useful output.

**Next objective:** Begin implementing the first Python component while learning the underlying programming concepts.

---

## 8. Planned Deliverables

- [ ] Functional Python system-monitoring application
- [ ] Organized and documented source code
- [ ] Installation and execution instructions
- [ ] Example monitoring output
- [ ] Tests for normal and abnormal conditions
- [ ] Development journal

---

## Project Philosophy

> **Remain Uncomfortable.**
>
> The objective is not simply to finish the project. It is to develop the ability to independently design, build, debug, and explain practical engineering solutions.

**Status:** Planning / Learning in Progress

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
