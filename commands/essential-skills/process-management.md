# Process Management

## `ps` - Display Running Processes

| Command   | Description                                        | Example        | Important Flags                                       |
|-----------|----------------------------------------------------|----------------|-------------------------------------------------------|
| `ps`      | Displays currently running processes.              | `ps`           | `aux`: Shows all processes for all users in a detailed format<br>`-e`: Displays all running processes<br>`-f`: Displays a full format with additional information |
| `ps aux`  | Shows detailed information about all running processes. | `ps aux`       |                                                       |
| `ps -e`   | Lists all running processes.                       | `ps -e`        |                                                       |
| `ps -f`   | Displays full-format output for each process.      | `ps -f`        |                                                       |

---

## `kill` - Terminate a Process

| Command      | Description                                             | Example               | Important Flags                             |
|--------------|---------------------------------------------------------|-----------------------|---------------------------------------------|
| `kill`       | Terminates a process by its PID.                        | `kill 1234`           | `-9`: Force kill (SIGKILL) for unresponsive processes<br>`-15`: Graceful termination (SIGTERM) (default) |
| `kill -9`    | Forcefully kills a process.                             | `kill -9 1234`        |                                             |
| `kill -15`   | Sends a termination signal to a process.                | `kill -15 1234`       |                                             |

---

## `jobs` - List Background Jobs

| Command   | Description                                         | Example    | Important Flags                              |
|-----------|-----------------------------------------------------|------------|----------------------------------------------|
| `jobs`    | Lists the current background jobs.                 | `jobs`     | `-l`: Displays additional job information (PID) |
| `jobs -l` | Lists background jobs with their process IDs (PIDs). | `jobs -l`  |                                              |
