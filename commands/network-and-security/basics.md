# Networking Basics in Linux

Linux provides a variety of commands to manage and troubleshoot networking, allowing you to view network configurations, check connectivity, and control network interfaces. Understanding these commands is essential for a system administrator or anyone managing Linux-based servers.

## Common Networking Commands

| Command      | Description                                                   | Example                                | Important Flags                                                                                                           |
| ------------ | ------------------------------------------------------------- | -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `ifconfig`   | Displays or configures network interfaces.                    | `ifconfig`                             | `-a`: Displays all interfaces (even if inactive).<br>`up`: Brings the interface up.<br>`down`: Brings the interface down. |
| `ip`         | Displays or configures network interfaces, routes, and more.  | `ip addr show`                         | `link`: Show the state of network interfaces.<br>`route`: Show the routing table.<br>`-s`: Display stats for interfaces.  |
| `ping`       | Sends ICMP echo requests to test network connectivity.        | `ping google.com`                      | `-c`: Number of ping requests to send.<br>`-i`: Interval between ping requests (in seconds).                              |
| `traceroute` | Displays the route packets take to a network host.            | `traceroute google.com`                | `-m`: Maximum number of hops.<br>`-w`: Timeout for each probe.                                                            |
| `nslookup`   | Queries DNS to obtain domain name or IP address mapping.      | `nslookup google.com`                  | `-type=A`: Query for A (address) record.<br>`-type=MX`: Query for mail exchange records.                                  |
| `dig`        | Queries DNS and shows detailed results.                       | `dig google.com`                       | `+short`: Display a shorter answer.<br>`+trace`: Show the query trace for the domain.                                     |
| `netstat`    | Displays network connections, routing tables, and statistics. | `netstat -tuln`                        | `-t`: Show TCP connections.<br>`-u`: Show UDP connections.<br>`-l`: Show only listening sockets.                          |
| `ss`         | Shows detailed information about network sockets.             | `ss -tuln`                             | `-t`: Show TCP sockets.<br>`-u`: Show UDP sockets.<br>`-n`: Show numerical addresses and ports.                           |
| `hostname`   | Displays or sets the system's hostname.                       | `hostname`                             | `-I`: Show all IP addresses assigned to the system.                                                                       |
| `curl`       | Transfers data from or to a server using various protocols.   | `curl -O https://example.com/file.zip` | `-O`: Save the file with its original name.<br>`-I`: Show the headers only.                                               |
| `wget`       | Downloads files from the web.                                 | `wget https://example.com/file.zip`    | `-c`: Resume a previous download.<br>`-P`: Set the download directory.                                                    |

---

## Conclusion

Linux provides a rich set of networking tools that help with managing, monitoring, and troubleshooting network-related issues. Understanding these commands is fundamental for a system administrator to effectively handle networking tasks on Linux-based systems.
