# Linux Fundamentals

A collection of Linux fundamentals learned while studying cybersecurity.

This document covers essential Linux commands used for navigating systems, viewing information, managing users, interacting with files, and using common shell operators.

---

# Finding Your Current Location

## Command

```bash
pwd
```

## Description

`pwd` stands for **Print Working Directory**.

It displays the full path of your current location within the Linux filesystem.

## Example

```bash
pwd
```

Example output:

```text
/home/user/Documents
```

## Cybersecurity Relevance

Knowing your current location is important when navigating systems during security assessments, investigations, and administration tasks.

---

# Listing Files and Directories

## Command

```bash
ls
```

## Description

The `ls` command lists the contents of the current directory.

## Useful Options

### Detailed Listing

```bash
ls -l
```

Displays additional information including:

* File permissions
* File owner
* File size
* Last modified date

Example:

```text
-rw-r--r-- 1 user user 1024 Jan 01 notes.txt
```

### Display Hidden Files

```bash
ls -la
```

Shows all files, including hidden files.

Linux hides files beginning with a `.` by default.

Example:

```text
.bashrc
```

Hidden files often contain configuration settings.

---

# Changing Directories

## Command

```bash
cd
```

## Description

The `cd` command allows you to change your current working directory.

## Example

Move into a directory:

```bash
cd Documents
```

Move back one directory:

```bash
cd ..
```

Return to your home directory:

```bash
cd ~
```

---

# Finding Files

## Command

```bash
find ~ -name filename
```

## Description

The `find` command searches for files and directories.

The example above searches from the user's home directory.

## Example

```bash
find ~ -name notes.txt
```

This searches for a file called `notes.txt`.

## Cybersecurity Relevance

During security assessments, `find` can be useful for locating:

* Configuration files
* Logs
* Sensitive files
* SSH keys
* Scripts

---

# Reading Files

## Command

```bash
cat filename.txt
```

## Description

The `cat` command displays the contents of a file directly in the terminal.

## Example

```bash
cat notes.txt
```

## Cybersecurity Relevance

Reading files is a common task during:

* System administration
* Incident response
* Penetration testing
* Log analysis

---

# Identifying the Current User

## Command

```bash
whoami
```

## Description

Displays the username of the current user.

## Example

```bash
whoami
```

Output:

```text
james
```

## Cybersecurity Relevance

Understanding user privileges is important when analysing systems and identifying potential privilege escalation paths.

---

# System Information

## Command

```bash
uname -a
```

## Description

Displays detailed information about the current system.

Information includes:

* Operating system
* Kernel version
* System architecture
* Host information

## Example

```bash
uname -a
```

To display only the operating system name:

```bash
uname
```

---

# Checking Disk Usage

## Command

```bash
df -h
```

## Description

The `df` command displays filesystem disk usage.

The `-h` option means **human-readable**, making sizes easier to understand.

Example:

```text
Filesystem      Size  Used  Available
/dev/root       20G   10G   10G
```

## Common Entries

| Entry           | Description                        |
| --------------- | ---------------------------------- |
| `/dev/root`     | Main system filesystem             |
| `tmpfs`         | Temporary filesystem stored in RAM |
| `/dev/shm`      | Shared memory filesystem           |
| `/run/user/UID` | Temporary user runtime files       |

---

# Linux Configuration Files

Linux stores many system configuration files inside:

```text
/etc
```

## Navigate to Configuration Files

```bash
cd /etc
```

View available files:

```bash
ls
```

Read a configuration file:

```bash
cat filename
```

## Cybersecurity Relevance

Configuration files may contain important information such as:

* System settings
* Service configurations
* User information
* Application settings

---

# SSH (Secure Shell)

## Command

```bash
ssh user@ip-address
```

## Description

SSH is a secure protocol used to remotely connect to another computer or server over a network.

## Example

```bash
ssh user@192.168.1.10
```

This connects to the device at `192.168.1.10` as the specified user.

## Cybersecurity Relevance

SSH is commonly used by:

* System administrators
* Security professionals
* Penetration testers

Understanding SSH is important for both securing and assessing systems.

---

# Viewing Command History

## Command

```bash
history
```

## Description

Displays previously executed commands by the current user.

## Example

```bash
history
```

## Cybersecurity Relevance

Command history can provide insight during investigations by showing previous activity performed on a system.

---

# Switching Users

## Command

```bash
su - username
```

## Description

The `su` command allows you to switch to another user account.

## Example

```bash
su - root
```

This attempts to switch to the root user.

A password may be required depending on the account permissions.

---

# Manual Pages

## Command

```bash
man command
```

## Description

The `man` command displays the manual page for a command, providing detailed information about its usage, options, and examples.

## Example

```bash
man nc
```

This displays the manual page for the `nc` command. Manual pages are available for most Linux commands.

---

# Echo Output

## Command

```bash
echo Hello World
```

## Description

The `echo` command prints text to the terminal.

## Example

```bash
echo Hello World
```

Output:

```text
Hello World
```

The `echo` command is also commonly used with output redirection to create or update files.

---

# Searching Files with Grep

## Command

```bash
grep "1.1.1.1" access.log
```

## Description

The `grep` command searches files for matching text or patterns.

Using the `-R` option allows recursive searching through directories.

## Example

```bash
grep -R "alex joined the server" server.log
```

This searches for the specified text within one or more files.

## Cybersecurity Relevance

`grep` is widely used to search:

* Log files
* Configuration files
* Source code
* Authentication logs
* Command output

---

# Shell Operators

Shell operators control how commands are executed or where their output is sent.

---

## Background Execution (`&`)

### Command

```bash
command &
```

### Description

The `&` operator runs a command in the background, allowing you to continue using the terminal while the command executes.

This is useful for long-running tasks.

### Example

```bash
cp largefile.iso /backup &
```

The file copy continues in the background while you can continue working.

## Cybersecurity Relevance

Running long scans or file operations in the background allows you to continue investigating systems without waiting for the task to complete.

---

## Conditional Execution (`&&`)

### Command

```bash
command1 && command2
```

### Description

The `&&` operator runs the second command only if the first command completes successfully.

This is useful when one command depends on another.

### Example

```bash
mkdir logs && cd logs
```

If the `logs` directory is successfully created, the terminal changes into it.

If the first command fails, the second command is not executed.

## Cybersecurity Relevance

This operator is frequently used in scripts and command chains where each step should only execute after the previous one succeeds.

---

## Output Redirection (`>`)

### Command

```bash
command > filename
```

### Description

The `>` operator redirects the output of a command into a file.

If the file already exists, its contents will be overwritten.

### Example

```bash
echo Hey > welcome.txt
```

Contents of `welcome.txt`:

```text
Hey
```

## Cybersecurity Relevance

Output redirection is useful for saving command results, scan output, logs, and reports for later analysis.

---

## Append Output (`>>`)

### Command

```bash
command >> filename
```

### Description

The `>>` operator appends the output of a command to the end of a file instead of replacing its existing contents.

### Example

Create the file:

```bash
echo Hey > welcome.txt
```

Append another line:

```bash
echo Hello >> welcome.txt
```

Contents of `welcome.txt`:

```text
Hey
Hello
```

Unlike `>`, the `>>` operator preserves any existing data within the file.

## Cybersecurity Relevance

Appending output is useful when recording logs, storing scan results, or documenting findings over time without losing previous information.

---

# Key Takeaways

* `pwd` shows your current location.
* `ls` lists files and directories.
* `cd` changes directories.
* `find` searches for files.
* `cat` reads file contents.
* `whoami` identifies the current user.
* `uname` provides system information.
* `df -h` displays disk usage.
* `/etc` contains important Linux configuration files.
* `ssh` provides secure remote access.
* `history` shows previous commands.
* `su` allows switching between user accounts.
* `man` displays manual pages for Linux commands.
* `echo` prints text to the terminal.
* `grep` searches files for matching text or patterns.
* `&` runs commands in the background.
* `&&` executes the next command only if the previous command succeeds.
* `>` redirects output to a file and overwrites existing contents.
* `>>` appends output to the end of a file.

---

# Future Topics

Upcoming Linux notes will cover:

* File permissions
* Users and groups
* Processes
* Services
* Networking
* Bash scripting
* Privilege escalation
