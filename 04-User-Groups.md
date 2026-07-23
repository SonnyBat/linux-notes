\# Users and Groups



This document covers the essential Linux commands used for managing users, groups, accounts, and user information on a Linux system.



\---



\# Viewing Current User



\## Command



```bash

whoami

```



\## Description



The `whoami` command displays the username of the currently logged-in user.



\## Example



```bash

whoami

```



Example output:



```text

kali

```



\## Cybersecurity Relevance



Knowing the current user account is important during system administration and security assessments because permissions and available actions depend on user privileges.



\---



\# Viewing User Information



\## Command



```bash

id

```



\## Description



The `id` command displays information about a user, including their user ID (UID), group ID (GID), and group memberships.



\## Example



```bash

id

```



Example output:



```text

uid=1000(kali) gid=1000(kali) groups=1000(kali),27(sudo)

```



\## Cybersecurity Relevance



Security professionals use `id` to identify account privileges and determine whether a user has elevated permissions.



\---



\# Viewing Logged-In Users



\## Command



```bash

who

```



\## Description



The `who` command shows users currently logged into the system.



\## Example



```bash

who

```



Example output:



```text

kali     pts/0        10.0.0.5

```



\## Cybersecurity Relevance



Monitoring logged-in users helps detect unauthorized access and suspicious activity on Linux systems.



\---



\# Creating Users



\## Command



```bash

useradd

```



\## Description



The `useradd` command creates a new user account on a Linux system.



\## Example



```bash

sudo useradd analyst

```



Creates a new user named `analyst`.



\## Cybersecurity Relevance



Managing user accounts securely is important for controlling access to systems and preventing unauthorized users.



\---



\# Changing User Passwords



\## Command



```bash

passwd

```



\## Description



The `passwd` command changes a user's password.



\## Example



```bash

sudo passwd analyst

```



Sets or changes the password for the `analyst` account.



\## Cybersecurity Relevance



Strong password management helps protect user accounts from unauthorized access.



\---



\# Creating Groups



\## Command



```bash

groupadd

```



\## Description



The `groupadd` command creates a new user group.



\## Example



```bash

sudo groupadd developers

```



Creates a group named `developers`.



\## Cybersecurity Relevance



Groups allow administrators to manage permissions efficiently by assigning access to multiple users at once.



\---



\# Adding Users to Groups



\## Command



```bash

usermod

```



\## Description



The `usermod` command modifies user account settings, including adding users to groups.



\## Example



```bash

sudo usermod -aG developers analyst

```



Adds the user `analyst` to the `developers` group.



\## Cybersecurity Relevance



Proper group management helps enforce the principle of least privilege by ensuring users only have necessary access.



\---



\# Key Takeaways



\- `whoami` displays the current user.

\- `id` shows user and group information.

\- `who` shows logged-in users.

\- `useradd` creates user accounts.

\- `passwd` manages passwords.

\- `groupadd` creates groups.

\- `usermod` modifies user group membership.



\---

