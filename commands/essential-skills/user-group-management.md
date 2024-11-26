# User and Group Management

Managing users and groups is crucial for access control and system organization in Linux. Below are the key commands for user and group management.

---

## User Management

| Command               | Description                                                    | Example                         | Important Flags                                                                                             |
|-----------------------|----------------------------------------------------------------|---------------------------------|-----------------------------------------------------------------------------------------------------------|
| `useradd <username>`   | Creates a new user account with default settings.              | `useradd john`                  | `-m`: Creates the user's home directory<br>`-s <shell>`: Specifies the login shell (e.g., `/bin/bash`)<br>`-c "<comment>"`: Adds a comment (e.g., full name) |
| `usermod <username>`   | Modifies an existing user account.                             | `usermod -aG sudo john`         | `-aG <group>`: Adds the user to a group without removing them from other groups<br>`-s <shell>`: Changes the user's login shell<br>`-d <dir>`: Changes the home directory |
| `userdel <username>`   | Deletes a user account.                                        | `userdel john`                  | `-r`: Removes the user's home directory and mail spool<br>`-f`: Forces the deletion of a user account if the user is logged in |
| `passwd <username>`    | Changes a user's password.                                     | `passwd john`                   | `-l`: Locks the user account<br>`-u`: Unlocks the user account<br>`-e`: Expire the user's password immediately<br>`-d`: Removes the user's password |
| `chage <username>`     | Changes a user's password expiry information.                 | `chage john`                    | `-M <days>`: Sets the maximum number of days before a password change is required<br>`-m <days>`: Sets the minimum number of days between password changes<br>`-I <days>`: Sets the number of days after password expiration to lock the account<br>`-l`: Displays password expiry information |
| `id <username>`        | Displays the user's ID and group ID information.               | `id john`                       | N/A                                                                                                       |

---

## Group Management

| Command               | Description                                                    | Example                         | Important Flags                                                                                             |
|-----------------------|----------------------------------------------------------------|---------------------------------|-----------------------------------------------------------------------------------------------------------|
| `groupadd <groupname>` | Creates a new group.                                           | `groupadd admins`               | `-g <GID>`: Specifies the group ID (GID)<br>`-f`: Forces the creation of the group even if it already exists |
| `groupdel <groupname>` | Deletes a group.                                               | `groupdel admins`               | N/A                                                                                                       |
| `usermod -aG <group>`  | Adds a user to a group.                                        | `usermod -aG sudo john`         | `-aG <group>`: Adds the user to the specified group without removing them from other groups |
| `gpasswd -a <user>`    | Adds a user to a group.                                        | `gpasswd -a john admins`       | N/A                                                                                                       |
| `gpasswd -d <user>`    | Removes a user from a group.                                   | `gpasswd -d john admins`       | N/A                                                                                                       |
| `groups <username>`    | Displays the groups a user belongs to.                         | `groups john`                   | N/A                                                                                                       |
