# File Management

This document covers the essential Linux commands used for creating, copying, moving, deleting, and identifying files and directories.

---

# Creating Files

## Command

```bash
touch filename
```

## Description

The `touch` command creates a new empty file.

If the file already exists, it updates its timestamp instead.

## Example

```bash
touch notes.txt
```

Creates an empty file named `notes.txt`.

## Cybersecurity Relevance

Creating files is useful for testing permissions, creating scripts, and storing notes or logs.

---

# Creating Directories

## Command

```bash
mkdir directory
```

## Description

The `mkdir` command creates a new directory.

## Example

```bash
mkdir Projects
```

Creates a directory named `Projects`.

---

# Copying Files and Directories

## Command

```bash
cp
```

## Description

The `cp` command copies files and directories.

Use the `-r` option when copying directories.

## Examples

Copy a file:

```bash
cp notes.txt backup.txt
```

Copy a directory:

```bash
cp -r Projects Backup
```

## Cybersecurity Relevance

Creating backups before editing files is common practice during investigations and system administration.

---

# Moving and Renaming Files

## Command

```bash
mv
```

## Description

The `mv` command moves files and directories.

It is also used to rename files.

## Examples

Move a file:

```bash
mv notes.txt Documents/
```

Rename a file:

```bash
mv notes.txt linux-notes.txt
```

---

# Removing Files and Directories

## Command

```bash
rm
```

## Description

The `rm` command removes files.

Use the `-r` option to remove directories and their contents.

## Examples

Delete a file:

```bash
rm notes.txt
```

Delete a directory:

```bash
rm -r Projects
```

> **Warning:** Files deleted with `rm` are not moved to a recycle bin and are typically difficult to recover.

## Cybersecurity Relevance

Understanding file deletion is important during system administration and forensic investigations.

---

# Reading Files

## Command

```bash
cat
```

## Description

The `cat` command displays the contents of a file.

## Example

```bash
cat notes.txt
```

## Cybersecurity Relevance

Viewing configuration files and logs is a common task during investigations and penetration testing.

---

# Identifying File Types

## Command

```bash
file
```

## Description

The `file` command determines the type of a file based on its contents rather than its extension.

## Example

```bash
file notes.txt
```

Example output:

```text
notes.txt: ASCII text
```

Another example:

```bash
file image.png
```

Output:

```text
image.png: PNG image data
```

## Cybersecurity Relevance

Attackers may disguise malicious files by changing their extensions. The `file` command helps identify the true file type.

---

# Key Takeaways

- `touch` creates empty files.
- `mkdir` creates directories.
- `cp` copies files and folders.
- `mv` moves or renames files.
- `rm` deletes files and directories.
- `cat` displays file contents.
- `file` identifies a file's true type.

---

