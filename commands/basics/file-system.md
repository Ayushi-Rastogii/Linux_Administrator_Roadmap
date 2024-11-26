# Navigating the File System

## `ls` - List Directory Contents

| Command  | Description                                           | Example  | Important Flags                                                                                                                                       |
| -------- | ----------------------------------------------------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ls`     | Lists files and directories in the current directory. | `ls`     | `-l`: Detailed listing<br>`-a`: Include hidden files<br>`-h`: Human-readable file sizes<br>`-R`: Recursive listing<br>`-t`: Sort by modification time |
| `ls -l`  | Detailed list of files and directories.               | `ls -l`  |                                                                                                                                                       |
| `ls -a`  | Shows all files, including hidden files.              | `ls -a`  |                                                                                                                                                       |
| `ls -lh` | Shows files with human-readable sizes.                | `ls -lh` |                                                                                                                                                       |
| `ls -R`  | Lists directories and contents recursively.           | `ls -R`  |                                                                                                                                                       |
| `ls -lt` | Sorts files by modification time, newest first.       | `ls -lt` |                                                                                                                                                       |

---

## `cd` - Change Directory

| Command        | Description                                          | Example                   | Important Flags                                                                |
| -------------- | ---------------------------------------------------- | ------------------------- | ------------------------------------------------------------------------------ |
| `cd`           | Changes the current directory.                       | `cd /home/user`           | `..`: Moves to the parent directory<br>`-`: Switches to the previous directory |
| `cd ..`        | Moves to the parent directory.                       | `cd ..`                   |                                                                                |
| `cd -`         | Switches to the previous directory.                  | `cd -`                    |                                                                                |
| `cd /path/`    | Move to a specific directory using an absolute path. | `cd /home/user/Documents` |                                                                                |
| `cd Documents` | Move to a directory using a relative path.           | `cd Documents`            |                                                                                |

---

## `pwd` - Print Working Directory

| Command | Description                                       | Example |
| ------- | ------------------------------------------------- | ------- |
| `pwd`   | Prints the current working directory (full path). | `pwd`   |

---

## `tree` - Display Directories in a Tree-like Format

| Command     | Description                                                 | Example           | Important Flags                                                                                                   |
| ----------- | ----------------------------------------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------- |
| `tree`      | Displays directories in a tree-like format.                 | `tree /home/user` | `-L <level>`: Limit depth of tree<br>`-d`: Only directories<br>`-a`: Include hidden files<br>`-f`: Show full path |
| `tree -L 2` | Displays a directory tree with a maximum depth of 2 levels. | `tree -L 2`       |                                                                                                                   |
| `tree -d`   | Lists directories only, excluding files.                    | `tree -d`         |                                                                                                                   |
| `tree -a`   | Includes hidden files in the directory tree.                | `tree -a`         |                                                                                                                   |
| `tree -f`   | Displays the full path for each file and directory.         | `tree -f`         |                                                                                                                   |

# File and Directory Management

## `mkdir` - Create a New Directory

| Command    | Description                             | Example                      | Important Flags                                                   |
| ---------- | --------------------------------------- | ---------------------------- | ----------------------------------------------------------------- |
| `mkdir`    | Creates a new directory.                | `mkdir my_folder`            | `-p`: Creates parent directories as needed (if they do not exist) |
| `mkdir -p` | Creates parent directories as required. | `mkdir -p /home/user/folder` |                                                                   |

---

## `rmdir` - Remove an Empty Directory

| Command    | Description                           | Example                      | Important Flags                                 |
| ---------- | ------------------------------------- | ---------------------------- | ----------------------------------------------- |
| `rmdir`    | Removes an empty directory.           | `rmdir my_folder`            | `-p`: Removes empty parent directories as well. |
| `rmdir -p` | Removes empty parent directories too. | `rmdir -p /home/user/folder` |                                                 |

---

## `rm` - Remove Files or Directories

| Command | Description                                   | Example          | Important Flags                                                                                                     |
| ------- | --------------------------------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------------- |
| `rm`    | Removes files or directories.                 | `rm file.txt`    | `-r`: Removes directories and their contents recursively<br>`-f`: Forces removal without prompting for confirmation |
| `rm -r` | Removes directories and contents recursively. | `rm -r folder`   | `-f`: Forces removal without confirmation                                                                           |
| `rm -f` | Forces removal without confirmation.          | `rm -f file.txt` |                                                                                                                     |

---

## `cp` - Copy Files or Directories

| Command | Description                                        | Example             | Important Flags                                                                         |
| ------- | -------------------------------------------------- | ------------------- | --------------------------------------------------------------------------------------- |
| `cp`    | Copies files or directories.                       | `cp file.txt /tmp`  | `-r`: Copies directories recursively<br>`-i`: Prompts before overwriting existing files |
| `cp -r` | Copies directories and their contents recursively. | `cp -r folder /tmp` |                                                                                         |

---

## `mv` - Move (or Rename) Files or Directories

| Command | Description                                | Example                      | Important Flags                                                                                                       |
| ------- | ------------------------------------------ | ---------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `mv`    | Moves or renames files or directories.     | `mv oldname.txt newname.txt` | `-i`: Prompts before overwriting existing files<br>`-u`: Moves files only if the source is newer than the destination |
| `mv -i` | Prompts before overwriting existing files. | `mv -i file.txt /tmp`        |                                                                                                                       |
| `mv -u` | Moves files only if the source is newer.   | `mv -u file.txt /tmp`        |                                                                                                                       |

# File Operations

## `cat` - Display Contents of a File

| Command | Description                      | Example        | Important Flags                                                             |
| ------- | -------------------------------- | -------------- | --------------------------------------------------------------------------- |
| `cat`   | Displays the contents of a file. | `cat file.txt` | `-n`: Numbers the lines of the output<br>`-b`: Numbers non-blank lines only |

---

## `nano/vim` - Edit a File in a Text Editor

| Command | Description                             | Example         | Important Flags                                                 |
| ------- | --------------------------------------- | --------------- | --------------------------------------------------------------- |
| `nano`  | Opens the file in the Nano text editor. | `nano file.txt` | `-w`: Disables line wrapping<br>`-B`: Backups before saving     |
| `vim`   | Opens the file in the Vim text editor.  | `vim file.txt`  | `:w`: Save changes<br>`:q`: Quit editor<br>`:wq`: Save and quit |

---

## `touch` - Create an Empty File

| Command | Description                                   | Example             | Important Flags                                                                   |
| ------- | --------------------------------------------- | ------------------- | --------------------------------------------------------------------------------- |
| `touch` | Creates a new empty file if it doesn't exist. | `touch newfile.txt` | `-c`: No change if the file exists<br>`-t`: Set a specific timestamp for the file |

---

## `head/tail` - Show the First/Last Few Lines of a File

| Command | Description                             | Example              | Important Flags                                                                                              |
| ------- | --------------------------------------- | -------------------- | ------------------------------------------------------------------------------------------------------------ |
| `head`  | Displays the first few lines of a file. | `head -n 5 file.txt` | `-n <num>`: Displays the first `<num>` lines (default is 10)                                                 |
| `tail`  | Displays the last few lines of a file.  | `tail -n 5 file.txt` | `-n <num>`: Displays the last `<num>` lines (default is 10)<br>`-f`: Follows the file as it grows (for logs) |

---

## `grep` - Search for a String in a File

| Command | Description                       | Example                | Important Flags                                                                                                                                    |
| ------- | --------------------------------- | ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `grep`  | Searches for a pattern in a file. | `grep "text" file.txt` | `-i`: Ignore case<br>`-r`: Search recursively in directories<br>`-l`: Print only the filenames that contain the pattern<br>`-n`: Show line numbers |

## `less` - Views a file page by page

| Command            | Description                                                | Example                      | Important Flags                                                                                                                               |
| ------------------ | ---------------------------------------------------------- | ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| `less <file>`      | Opens a file and allows the user to view it page by page.  | `less largefile.txt`         | `-N`: Displays line numbers<br>`-S`: Truncates long lines without wrapping<br>`-F`: Automatically exits if the entire file fits on one screen |
| `less +F <file>`   | Continuously scrolls to the end of a file, like `tail -f`. | `less +F largefile.txt`      | `-R`: Allows raw control characters (e.g., colors) to be displayed                                                                            |
| `less -i <file>`   | Makes the search case-insensitive.                         | `less -i largefile.txt`      | `-I`: Ignores case for searching<br>`-p <pattern>`: Starts at the first match of the pattern                                                  |
| `less +/<pattern>` | Searches for a pattern in the file while opening it.       | `less +/error largefile.txt` | `-G`: Highlights the search results                                                                                                           |

---

## `more` - Views a file one screen at a time

| Command        | Description                                       | Example                  | Important Flags                                                                                    |
| -------------- | ------------------------------------------------- | ------------------------ | -------------------------------------------------------------------------------------------------- |
| `more <file>`  | Views a file one screen at a time.                | `more largefile.txt`     | `-c`: Clears the screen before displaying the file<br>`-s`: Squeezes multiple blank lines into one |
| `more +<line>` | Starts displaying the file from a specified line. | `more +10 largefile.txt` | `-d`: Prompts the user before scrolling<br>`-p`: Allows the user to search through the file        |
