# System Information

## `whoami` - Display the Current User

| Command  | Description                          | Example  | Important Flags |
| -------- | ------------------------------------ | -------- | --------------- |
| `whoami` | Displays the current logged-in user. | `whoami` | N/A             |

---

## `hostname` - Display or Set the System's Hostname

| Command       | Description                             | Example       | Important Flags                                                                                      |
| ------------- | --------------------------------------- | ------------- | ---------------------------------------------------------------------------------------------------- |
| `hostname`    | Displays the system's hostname.         | `hostname`    | `-I`: Show all IP addresses associated with the hostname<br>`-s`: Display short hostname (no domain) |
| `hostname -I` | Shows the IP address(es) of the system. | `hostname -I` |                                                                                                      |

---

## `which` - Show the Full Path of Shell Commands

| Command | Description                                     | Example        | Important Flags |
| ------- | ----------------------------------------------- | -------------- | --------------- |
| `which` | Shows the full path of a command or executable. | `which python` | N/A             |

---

## `uname` - Print System Information

| Command | Description                        | Example | Important Flags                                                                                 |
| ------- | ---------------------------------- | ------- | ----------------------------------------------------------------------------------------------- |
| `uname` | Displays basic system information. | `uname` | `-a`: Displays all system information (kernel, hostname, etc.)<br>`-r`: Displays kernel version |

## Useful Tips

Use man <command> to get detailed information about any command:

```bash
man ls
```

Combine commands using pipes (|) to perform advanced operations

```bash
ls -l | grep ".txt"
```
