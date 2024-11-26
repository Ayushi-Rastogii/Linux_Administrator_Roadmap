# Memory Management

## `free` - Display Memory Usage

| Command   | Description                         | Example   | Important Flags                                                                          |
| --------- | ----------------------------------- | --------- | ---------------------------------------------------------------------------------------- |
| `free`    | Displays memory usage.              | `free`    | `-m`: Shows memory usage in megabytes (MB)<br>`-g`: Shows memory usage in gigabytes (GB) |
| `free -m` | Displays memory usage in megabytes. | `free -m` |                                                                                          |

---

# System Monitoring

## `df` - Check Disk Space Usage

| Command | Description                                     | Example | Important Flags                                                               |
| ------- | ----------------------------------------------- | ------- | ----------------------------------------------------------------------------- |
| `df`    | Displays disk space usage.                      | `df`    | `-h`: Human-readable format (e.g., MB, GB)<br>`-T`: Displays file system type |
| `df -h` | Displays disk space in a human-readable format. | `df -h` |                                                                               |

---

## `uptime` - Show System Uptime and Load Averages

| Command  | Description                            | Example  | Important Flags                                                        |
| -------- | -------------------------------------- | -------- | ---------------------------------------------------------------------- |
| `uptime` | Shows system uptime and load averages. | `uptime` | `-p`: Displays uptime in a readable format (e.g., 2 hours, 30 minutes) |

---

## `top` - Show Real-Time Processes and Resource Usage

| Command  | Description                                      | Example       | Important Flags                                                                                            |
| -------- | ------------------------------------------------ | ------------- | ---------------------------------------------------------------------------------------------------------- |
| `top`    | Displays real-time processes and resource usage. | `top`         | `-u <user>`: Show processes for a specific user<br>`-d <seconds>`: Refreshes the display every `<seconds>` |
| `top -u` | Shows processes for a specific user.             | `top -u user` |                                                                                                            |
