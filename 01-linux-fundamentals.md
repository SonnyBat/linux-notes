# Linux Fundamentals

A collection of Linux fundamentals learned while studying cybersecurity.

This document covers essential Linux commands used for navigating systems, viewing information, managing users, and interacting with files.

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

- File permissions
- File owner
- File size
- Last modified date

Example:

```text
-rw-r--r-- 1 user user 1024 Jan 01 notes.txt
```

---

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

- Configuration files
- Logs
- Sensitive files
- SSH keys
- Scripts

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

- System administration
- Incident response
- Penetration testing
- Log analysis

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

- Operating system
- Kernel version
- System architecture
- Host information

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

| Entry | Description |
|---|---|
| `/dev/root` | Main system filesystem |
| `tmpfs` | Temporary filesystem stored in RAM |
| `/dev/shm` | Shared memory filesystem |
| `/run/user/UID` | Temporary user runtime files |

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

- System settings
- Service configurations
- User information
- Application settings

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

- System administrators
- Security professionals
- Penetration testers

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

# Key Takeaways

- `pwd` shows your current location.
- `ls` lists files and directories.
- `cd` changes directories.
- `find` searches for files.
- `cat` reads file contents.
- `whoami` identifies the current user.
- `uname` provides system information.
- `df -h` displays disk usage.
- `/etc` contains important Linux configuration files.
- `ssh` provides secure remote access.
- `history` shows previous commands.
- `su` allows switching between user accounts.

---

# Future Topics

Upcoming Linux notes will cover:

- File permissions
- Users and groups
- Processes
- Services
- Networking
- Bash scripting
- Privilege escalation