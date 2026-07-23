# Permissions

This document covers the essential Linux commands used for managing file permissions, ownership, and access control.

---

# Viewing File Permissions

## Command

```bash
ls -l
```

## Description

The `ls -l` command displays detailed information about files and directories, including ownership and permissions.

## Example

```bash
ls -l notes.txt
```

Example output:

```text
-rw-r--r-- 1 kali kali 120 notes.txt
```

## Cybersecurity Relevance

Understanding file permissions helps identify security weaknesses caused by incorrect access settings.

---

# Changing Permissions

## Command

```bash
chmod
```

## Description

The `chmod` command changes the permissions of files and directories.

## Example

```bash
chmod 755 script.sh
```

Gives the owner full permissions and allows others to read and execute the file.

Another example:

```bash
chmod +x script.sh
```

Makes a file executable.

## Cybersecurity Relevance

Incorrect permissions can expose sensitive files or allow unauthorized users to modify important system files.

---

# Changing File Ownership

## Command

```bash
chown
```

## Description

The `chown` command changes the owner and group of a file or directory.

## Example

```bash
sudo chown user file.txt
```

Changes the owner of `file.txt` to `user`.

Another example:

```bash
sudo chown user:developers file.txt
```

Changes both the owner and group.

## Cybersecurity Relevance

Ownership controls who manages files. Incorrect ownership can lead to privilege escalation risks.

---

# Changing Group Ownership

## Command

```bash
chgrp
```

## Description

The `chgrp` command changes the group ownership of a file or directory.

## Example

```bash
sudo chgrp developers notes.txt
```

Changes the group ownership of `notes.txt`.

## Cybersecurity Relevance

Proper group ownership ensures users only have access to resources they are authorized to use.

---

# Viewing Current Permissions

## Command

```bash
stat
```

## Description

The `stat` command displays detailed information about a file, including permissions, ownership, and timestamps.

## Example

```bash
stat notes.txt
```

## Cybersecurity Relevance

Security professionals use `stat` to investigate file metadata and identify suspicious changes.

---

# Key Takeaways

- `ls -l` displays file permissions.
- `chmod` changes file permissions.
- `chown` changes file ownership.
- `chgrp` changes group ownership.
- `stat` displays detailed file information.

---