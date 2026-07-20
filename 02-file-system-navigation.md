# File System Navigation

This document covers the essential Linux commands used for navigating the filesystem and locating files.

---

# Print Working Directory

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

Output:

```text
/home/user/Documents
```

## Cybersecurity Relevance

Knowing your current location is essential during system administration, incident response, and penetration testing.

---

# Listing Files and Directories

## Command

```bash
ls
```

## Description

The `ls` command lists the contents of the current directory.

## Example

```bash
ls
```

---

## Detailed Listing

### Command

```bash
ls -l
```

### Description

Displays additional information about files and directories.

Information includes:

- File permissions
- Number of links
- File owner
- Group owner
- File size
- Last modified date

Example:

```text
-rw-r--r-- 1 user user 2048 Jan 10 notes.txt
```

---

## Display Hidden Files

### Command

```bash
ls -la
```

### Description

Shows all files, including hidden files.

Linux hides files beginning with a `.` by default.

Example:

```text
.bashrc
.profile
```

Hidden files often store user or application configuration.

---

# Changing Directories

## Command

```bash
cd
```

## Description

The `cd` command changes your current working directory.

## Examples

Move into a directory:

```bash
cd Documents
```

Move up one directory:

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
find
```

## Description

The `find` command searches for files and directories.

## Example

```bash
find ~ -name notes.txt
```

This searches your home directory for a file named `notes.txt`.

## Cybersecurity Relevance

The `find` command is useful for locating:

- Configuration files
- Log files
- SSH keys
- Scripts
- Sensitive documents

---

# Searching File Contents

## Command

```bash
grep
```

## Description

The `grep` command searches files for matching text or patterns.

## Example

```bash
grep "Failed password" auth.log
```

Search recursively through directories:

```bash
grep -R "password" .
```

## Cybersecurity Relevance

`grep` is commonly used to search:

- System logs
- Configuration files
- Source code
- Authentication logs

---

# Key Takeaways

- `pwd` displays your current directory.
- `ls` lists files and folders.
- `ls -l` provides a detailed file listing.
- `ls -la` displays hidden files.
- `cd` changes directories.
- `find` searches for files and folders.
- `grep` searches files for matching text.

---
