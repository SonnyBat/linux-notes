# Processes

This document covers the essential Linux commands used for viewing, managing, and controlling running processes.

---

# Viewing Processes

## Command

```bash
ps
```

## Description

The `ps` command displays information about currently running processes.

## Example

```bash
ps
```

Example output:

```text
PID TTY          TIME CMD
1234 pts/0    00:00:01 bash
```

## Cybersecurity Relevance

Viewing processes helps security professionals identify suspicious programs, investigate system activity, and monitor running services.

---

# Viewing All Processes

## Command

```bash
ps aux
```

## Description

The `ps aux` command displays all running processes for every user.

## Example

```bash
ps aux
```

## Cybersecurity Relevance

Attackers may hide malicious processes on compromised systems. Reviewing running processes helps detect unusual activity.

---

# Monitoring Processes in Real Time

## Command

```bash
top
```

## Description

The `top` command provides a real-time view of running processes, CPU usage, memory usage, and system activity.

## Example

```bash
top
```

## Cybersecurity Relevance

Monitoring system resources can help identify abnormal processes consuming excessive CPU or memory.

---

# Ending Processes

## Command

```bash
kill
```

## Description

The `kill` command sends a signal to a process to stop or control it.

## Example

```bash
kill 1234
```

Stops the process with PID `1234`.

## Cybersecurity Relevance

Administrators use `kill` to stop unwanted or malicious processes during incident response.

---

# Finding Process IDs

## Command

```bash
pgrep
```

## Description

The `pgrep` command searches for processes by name and returns their process IDs.

## Example

```bash
pgrep firefox
```

Example output:

```text
2456
```

## Cybersecurity Relevance

Finding process IDs quickly allows administrators to investigate or terminate suspicious applications.

---

# Running Processes in Background

## Command

```bash
&
```

## Description

Adding `&` to a command runs it as a background process.

## Example

```bash
ping google.com &
```

Runs the ping command in the background.

## Cybersecurity Relevance

Understanding background processes helps security professionals analyze system behavior and manage running tasks.

---

# Key Takeaways

- `ps` displays running processes.
- `ps aux` shows all processes.
- `top` monitors processes in real time.
- `kill` stops processes.
- `pgrep` finds process IDs.
- `&` runs commands in the background.

---