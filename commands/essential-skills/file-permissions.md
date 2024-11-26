# File Permissions Management

File permissions in Linux are essential for controlling access to files and directories. Linux uses three types of permissions (read, write, and execute) and assigns them to the file owner, group, and others. Below are the essential commands for managing file permissions.

---

## Viewing and Understanding File Permissions

| Command       | Description                                                        | Example         | Important Flags                                    |
| ------------- | ------------------------------------------------------------------ | --------------- | -------------------------------------------------- |
| `ls -l`       | Lists files and directories with detailed permissions.             | `ls -l`         | N/A                                                |
| `ls -lh`      | Lists files with human-readable file sizes and permissions.        | `ls -lh`        | `-h`: Human-readable file sizes (e.g., KB, MB, GB) |
| `stat <file>` | Displays detailed information about a file, including permissions. | `stat file.txt` | N/A                                                |

---

## Changing File Permissions

| Command                        | Description                                               | Example                   | Important Flags                                                                                                      |
| ------------------------------ | --------------------------------------------------------- | ------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `chmod <permissions> <file>`   | Changes the permissions of a file.                        | `chmod 755 file.txt`      | `r`: Read, `w`: Write, `x`: Execute<br>Use octal notation (e.g., 755, 644)<br>Use symbolic notation (e.g., u+x, g-w) |
| `chmod +x <file>`              | Adds execute permission to a file.                        | `chmod +x script.sh`      | `+x`: Adds execute permission<br>`-x`: Removes execute permission                                                    |
| `chmod -R <permissions> <dir>` | Recursively changes permissions of files and directories. | `chmod -R 755 /home/user` | `-R`: Recursive change                                                                                               |
| `chmod u+x <file>`             | Adds execute permission for the file owner (user).        | `chmod u+x file.sh`       | `u`: User (file owner)<br>`g`: Group<br>`o`: Others                                                                  |
| `chmod g-w <file>`             | Removes write permission from the group.                  | `chmod g-w file.txt`      | `u+x`: Adds execute permission for user<br>`g+w`: Adds write permission for group                                    |

---

## Changing File Ownership

| Command                         | Description                                                        | Example                           | Important Flags        |
| ------------------------------- | ------------------------------------------------------------------ | --------------------------------- | ---------------------- |
| `chown <user>:<group> <file>`   | Changes the ownership of a file or directory.                      | `chown john:admins file.txt`      | N/A                    |
| `chown -R <user>:<group> <dir>` | Recursively changes ownership of files and directories.            | `chown -R john:admins /home/john` | `-R`: Recursive change |
| `chown <user> <file>`           | Changes the file owner.                                            | `chown john file.txt`             | N/A                    |
| `chgrp <group> <file>`          | Changes the group ownership of a file.                             | `chgrp admins file.txt`           | N/A                    |
| `chown :<group> <file>`         | Changes the group ownership of a file, leaving the user unchanged. | `chown :admins file.txt`          | N/A                    |

---

## Special Permissions

| Command           | Description                                             | Example                    | Important Flags                                                   |
| ----------------- | ------------------------------------------------------- | -------------------------- | ----------------------------------------------------------------- |
| `chmod +s <file>` | Sets the SUID (Set User ID) permission on a file.       | `chmod +s /usr/bin/passwd` | `+s`: Set the SUID permission<br>`-s`: Remove the SUID permission |
| `chmod +s <dir>`  | Sets the SGID (Set Group ID) permission on a directory. | `chmod +s /data/uploads`   | `+s`: Set the SGID permission                                     |
| `chmod +t <dir>`  | Sets the Sticky Bit on a directory.                     | `chmod +t /tmp`            | `+t`: Set the sticky bit<br>`-t`: Remove the sticky bit           |

---

## File Permissions Notation

### Numeric Notation

| Permission | Numeric Value |
| ---------- | ------------- |
| `r`        | 4             |
| `w`        | 2             |
| `x`        | 1             |
| `-`        | 0             |

- The permissions are represented by three digits, each representing the owner, group, and others.
- For example, `755` translates to `rwxr-xr-x`, where:
  - `rwx` is the owner's permissions (read, write, execute).
  - `r-x` is the group's permissions (read, execute).
  - `r-x` is others' permissions (read, execute).

### Symbolic Notation

| Permission | Symbol         |
| ---------- | -------------- |
| `r`        | `read`         |
| `w`        | `write`        |
| `x`        | `execute`      |
| `u`        | `user` (owner) |
| `g`        | `group`        |
| `o`        | `others`       |

- You can use symbolic notation to add or remove permissions:
  - `chmod u+x file.txt`: Adds execute permission for the user.
  - `chmod g-w file.txt`: Removes write permission for the group.
  - `chmod o=r file.txt`: Sets read-only permission for others.

---

## Understanding Special Permissions

| Permission   | Description                                                                | Example                      |
| ------------ | -------------------------------------------------------------------------- | ---------------------------- |
| `SUID`       | Allows a user to run an executable with the permissions of the file owner. | `chmod +s /usr/bin/passwd`   |
| `SGID`       | Allows a user to run an executable with the permissions of the group.      | `chmod +s /home/user/upload` |
| `Sticky Bit` | Restricts file deletion in a directory to the file owner or root.          | `chmod +t /tmp`              |

---

By understanding these commands and flags, you'll have full control over the file permissions and ownership in your Linux system.
