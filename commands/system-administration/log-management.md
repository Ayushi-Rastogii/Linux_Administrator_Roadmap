# Log Management in Linux

In Linux, **Log Management** refers to the processes involved in monitoring, analyzing, and managing system logs. System logs are essential for troubleshooting, monitoring system health, and ensuring security.

## Key Log Files in Linux

- **/var/log/syslog** – General system log file, stores system activity.
- **/var/log/auth.log** – Authentication-related events, useful for tracking login attempts.
- **/var/log/dmesg** – Boot-time kernel log messages.
- **/var/log/kern.log** – Kernel logs that provide information about the Linux kernel.
- **/var/log/boot.log** – Logs related to the system boot process.

## Common Log Management Commands:

| Command      | Description                                                    | Example                         | Important Flags                                                              |
| ------------ | -------------------------------------------------------------- | ------------------------------- | ---------------------------------------------------------------------------- |
| `dmesg`      | Displays boot-related messages from the kernel.                | `dmesg`                         | `-T`: Prints timestamp in human-readable format.                             |
| `journalctl` | Queries and displays logs from the systemd journal.            | `journalctl`                    | `-xe`: Displays logs with extended info.<br>`-f`: Follows logs in real-time. |
| `tail`       | Shows the last part of the log file.                           | `tail -n 10 /var/log/syslog`    | `-f`: Follows the log in real-time.<br>`-n`: Specifies the number of lines.  |
| `less`       | Allows scrolling through large log files.                      | `less /var/log/syslog`          | `-S`: Disables line wrapping.<br>`-N`: Shows line numbers.                   |
| `cat`        | Displays the contents of a log file.                           | `cat /var/log/auth.log`         |                                                                              |
| `logrotate`  | Manages the rotation of log files, keeping log sizes in check. | `logrotate /etc/logrotate.conf` | `-f`: Forces log rotation.                                                   |

## Log Rotation

Log rotation ensures that logs do not consume too much disk space by rotating older logs into compressed files. It can be configured in `/etc/logrotate.conf` and individual files in `/etc/logrotate.d/`.

### Example Logrotate Configuration:

```bash
/var/log/syslog {
    weekly
    rotate 4
    compress
    missingok
    notifempty
}
```
