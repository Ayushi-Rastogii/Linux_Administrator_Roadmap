# Package Management

## `apt` - Package Management for Debian-based Distributions

| Command            | Description                                                                                                                    | Example             | Important Flags                                                                                                                                                                              |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `apt update`       | Updates the list of available packages.                                                                                        | `apt update`        | N/A                                                                                                                                                                                          |
| `apt upgrade`      | Installs the latest versions of all packages.                                                                                  | `apt upgrade`       | `-y`: Automatically answers yes to prompts                                                                                                                                                   |
| `apt install`      | Installs a package.                                                                                                            | `apt install <pkg>` | `-y`: Automatically answers yes to prompts<br> `-f`: Fixes broken dependencies if any when used with -y <br>`--no-install-recommends`: Installs the package without recommended dependencies |
| `apt remove`       | Removes a package.                                                                                                             | `apt remove <pkg>`  | `-y`: Automatically answers yes to prompts <br> `--auto-remove` : Removes unnecessary dependencies automatically.                                                                            |
| `apt search`       | Searches for a package by name.                                                                                                | `apt search <pkg>`  | `--names-only`: Search only package names<br> `--installed`: Searches only among the installed packages.<br> `-f`: Find matching packages, including description when used with --installed. |
| `apt list`         | Lists all packages that are available for installation or are installed.                                                       | `apt list`          | `--installed`: Lists installed packages only<br> `--upgradable`: Lists packages that can be upgraded when used with --installed                                                              |
| `apt show`         | Displays detailed information about a package.                                                                                 | `apt show <pkg>`    | N/A                                                                                                                                                                                          |
| `apt autoremove`   | Removes unused packages that were automatically installed to satisfy dependencies for other packages and are no longer needed. | `apt autoremove`    | `-y`:Automatically removes unused packages without prompting.                                                                                                                                |
| `apt full-upgrade` | Installs/upgrades/removes packages as necessary to complete the upgrade.                                                       | `apt full-upgrade`  | `-y`: Automatically answers 'yes' to all prompts                                                                                                                                             |

---

## Example Workflow

1. **Update Package List**:  
   `sudo apt update`

2. **Upgrade Installed Packages**:  
   `sudo apt upgrade -y`

3. **Install a Package**:  
   `sudo apt install vim -y`

4. **Remove a Package**:  
   `sudo apt remove vim -y`

5. **Search for a Package**:  
   `apt search vim`

6. **Display Information about a Package**:  
   `apt show vim`

7. **Remove Unused Dependencies**:  
   `sudo apt autoremove`

---

### Summary of Key Flags:

- **`-y`**: Automatically answers 'yes' to prompts (use with care).
- **`--no-install-recommends`**: Installs a package without recommended dependencies.
- **`--purge`**: Removes the package and its configuration files.
- **`--installed`**: Only lists or searches installed packages.
- **`--upgradable`**: Lists upgradable packages.
- **`-f`**: Fixes broken dependencies.
- **`--names-only`**: Searches only package names, not descriptions.
- **`--auto-remove`**: Automatically removes unused dependencies.

---

## `yum` - Package Management for RHEL/CentOS-based Distributions

| Command       | Description                             | Example              | Important Flags                            |
| ------------- | --------------------------------------- | -------------------- | ------------------------------------------ |
| `yum update`  | Updates the list of available packages. | `yum update`         | `-y`: Automatically answers yes to prompts |
| `yum install` | Installs a package.                     | `yum install <pkg>`  | `-y`: Automatically answers yes to prompts |
| `yum remove`  | Removes a package.                      | `yum remove <pkg>`   | `-y`: Automatically answers yes to prompts |
| `yum search`  | Searches for a package by name.         | `yum search <pkg>`   |                                            |
| `yum list`    | Lists installed packages.               | `yum list installed` |                                            |

---

## `dnf` - Package Management for newer RHEL/CentOS/Fedora

| Command       | Description                             | Example              | Important Flags                            |
| ------------- | --------------------------------------- | -------------------- | ------------------------------------------ |
| `dnf update`  | Updates the list of available packages. | `dnf update`         | `-y`: Automatically answers yes to prompts |
| `dnf install` | Installs a package.                     | `dnf install <pkg>`  | `-y`: Automatically answers yes to prompts |
| `dnf remove`  | Removes a package.                      | `dnf remove <pkg>`   | `-y`: Automatically answers yes to prompts |
| `dnf search`  | Searches for a package by name.         | `dnf search <pkg>`   |                                            |
| `dnf list`    | Lists installed packages.               | `dnf list installed` |                                            |

---

## `rpm` - RPM Package Management for RHEL/CentOS/Fedora

| Command  | Description                                     | Example            | Important Flags                                |
| -------- | ----------------------------------------------- | ------------------ | ---------------------------------------------- |
| `rpm -i` | Installs an RPM package.                        | `rpm -i <pkg.rpm>` |                                                |
| `rpm -e` | Removes an RPM package.                         | `rpm -e <pkg>`     |                                                |
| `rpm -q` | Queries information about an installed package. | `rpm -q <pkg>`     | `-l`: Lists all files installed by the package |
| `rpm -U` | Upgrades an installed RPM package.              | `rpm -U <pkg.rpm>` |                                                |
| `rpm -V` | Verifies the installation of a package.         | `rpm -V <pkg>`     |                                                |

---

## `snap` - Package Management for Snaps (Universal Packages)

| Command        | Description                      | Example              | Important Flags                             |
| -------------- | -------------------------------- | -------------------- | ------------------------------------------- |
| `snap install` | Installs a snap package.         | `snap install <pkg>` | `--classic`: Install in classic confinement |
| `snap remove`  | Removes a snap package.          | `snap remove <pkg>`  |                                             |
| `snap list`    | Lists installed snap packages.   | `snap list`          |                                             |
| `snap refresh` | Updates installed snap packages. | `snap refresh`       |                                             |

---

## `pacman` - Package Management for Arch Linux

| Command       | Description                                                  | Example            | Important Flags                               |
| ------------- | ------------------------------------------------------------ | ------------------ | --------------------------------------------- |
| `pacman -Syu` | Synchronizes the package database and upgrades all packages. | `pacman -Syu`      | `-y`: Automatically answers yes to prompts    |
| `pacman -S`   | Installs a package.                                          | `pacman -S <pkg>`  | `--noconfirm`: Skips prompts for confirmation |
| `pacman -R`   | Removes a package.                                           | `pacman -R <pkg>`  |                                               |
| `pacman -Ss`  | Searches for a package.                                      | `pacman -Ss <pkg>` |                                               |
| `pacman -Qi`  | Queries information about an installed package.              | `pacman -Qi <pkg>` |                                               |
