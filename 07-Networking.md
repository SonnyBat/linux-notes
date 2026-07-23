# Networking

This document covers the essential Linux commands used for network communication, connectivity testing, remote access, and transferring files between systems.

---

# Testing Network Connectivity

## Command

```bash
ping
```

## Description

The `ping` command tests whether a device is reachable over a network by sending ICMP echo requests and measuring the response time.

## Example

```bash
ping google.com
```

Example output:

```text
64 bytes from google.com: icmp_seq=1 ttl=117 time=12.4 ms
```

## Cybersecurity Relevance

The `ping` command is commonly used during reconnaissance to determine whether hosts are active and reachable on a network. Security professionals use it to troubleshoot connectivity and identify potential targets during authorized assessments.

---

# Downloading Files

## Command

```bash
wget
```

## Description

The `wget` command downloads files from web servers using protocols such as HTTP, HTTPS, and FTP.

## Example

```bash
wget https://example.com/file.txt
```

Downloads `file.txt` from the specified URL.

Another example:

```bash
wget -O notes.txt https://example.com/data.txt
```

Saves the downloaded file with a custom name.

## Cybersecurity Relevance

Security professionals use `wget` to retrieve tools, scripts, and files from trusted sources during system administration and testing. Attackers may also abuse download utilities to retrieve malicious files, so monitoring unexpected downloads is important.

---

# Secure Remote Access

## Command

```bash
ssh
```

## Description

The `ssh` command creates a secure remote connection to another Linux system over an encrypted connection.

## Example

```bash
ssh user@192.168.1.10
```

Connects to a remote machine using the specified username and IP address.

Another example:

```bash
ssh user@example.com
```

Connects to a remote server using its hostname.

## Cybersecurity Relevance

SSH is widely used by system administrators and security professionals to securely manage remote servers. Misconfigured SSH services are commonly targeted by attackers, making strong passwords, key authentication, and proper configuration important security practices.

---

# Secure File Transfer

## Command

```bash
scp
```

## Description

The `scp` command securely copies files between local and remote systems using SSH encryption.

## Example

Copy a file to a remote system:

```bash
scp notes.txt user@192.168.1.10:/home/user/
```

Copy a file from a remote system:

```bash
scp user@192.168.1.10:/home/user/notes.txt .
```

## Cybersecurity Relevance

The `scp` command is used by administrators and security professionals to securely transfer files, backups, scripts, and evidence during investigations. Because it uses SSH encryption, transferred data is protected from interception.

---

# Key Takeaways

- `ping` tests network connectivity between devices.
- `wget` downloads files from online sources.
- `ssh` provides secure remote access to Linux systems.
- `scp` securely transfers files between machines.

---