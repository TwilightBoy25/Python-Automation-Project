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
