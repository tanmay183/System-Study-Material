## ✅ `pwd` and `cd` Command Reference Table (Support-Focused)

| 🔢 No | ✅ Command         | 💡 Explanation                                                       | 📁 Example        | 🛠️ Use Case in Support Domain                                     |
| ----- | ----------------- | -------------------------------------------------------------------- | ----------------- | ------------------------------------------------------------------ |
| 1     | `pwd`             | Print the **current working directory**                              | `pwd`             | Know your current location before running critical commands        |
| 2     | `cd`              | Change to **home directory** of the current user                     | `cd`              | Reset to base directory before navigating                          |
| 3     | `cd /path/to/dir` | Change to a specific directory by **absolute path**                  | `cd /var/log/app` | Move to log/config/scripts directory                               |
| 4     | `cd ..`           | Move **one level up** from current directory                         | `cd ..`           | Quickly backtrack in folder structure                              |
| 5     | `cd ../..`        | Move **two levels up**                                               | `cd ../..`        | Navigate from nested folders                                       |
| 6     | `cd -`            | Switch to the **last visited directory**                             | `cd -`            | Toggle between two directories (very useful in log/script jumping) |
| 7     | `cd ~`            | Go to the **home directory**                                         | `cd ~`            | Reset from deep path to home quickly                               |
| 8     | `cd ./dir`        | Change directory using **relative path** from current location       | `cd ./scripts`    | Enter subfolders without full path                                 |
| 9     | `cd /`            | Go to **root directory**                                             | `cd /`            | Start exploring filesystem from the top                            |
| 10    | `cd "$VAR"`       | Change directory using a **variable**                                | `cd "$LOG_DIR"`   | Use in shell scripts for dynamic pathing                           |
| 11    | `pwd -P`          | Print the **physical path**, resolving symbolic links                | `pwd -P`          | Ensures accurate path when symlinks are involved                   |
| 12    | `pwd -L`          | Print the **logical path** (default behavior, even through symlinks) | `pwd -L`          | When navigating via symlinks, show logical location                |
| 13    | `cd --`           | Resets to home directory (like `cd`)                                 | `cd --`           | Same as `cd`, but useful in scripts                                |

---

## 🛠️ Real Support Use Cases:

| 💡 Task                                      | 🔧 Command Example               | 🛠️ Explanation                                                            |
| -------------------------------------------- | -------------------------------- | -------------------------------------------------------------------------- |
| Navigate to logs folder and confirm location | `cd /var/log/app` → `pwd`        | Helps ensure you are in the correct path before deleting or analyzing logs |
| Move between two important folders quickly   | `cd /logs && cd -`               | Jump between current logs and backup logs                                  |
| Navigate back after inspecting a config file | `cd /etc/myapp/conf && cd -`     | Fast toggle between source and config folder                               |
| Start a script from script directory         | `cd /opt/scripts && ./runJob.sh` | Go to script location before execution                                     |







## ✅ `mkdir` Command Reference Table (Support-Focused)

| 🔢 No | ✅ Command                  | 💡 Explanation                                                | 📁 Example                       | 🛠️ Use Case in Support Domain                             |
| ----- | -------------------------- | ------------------------------------------------------------- | -------------------------------- | ---------------------------------------------------------- |
| 1     | `mkdir dirname`            | Create a single new directory in current location             | `mkdir logs`                     | Create a folder to store logs manually                     |
| 2     | `mkdir /path/to/dir`       | Create directory at an **absolute path**                      | `mkdir /opt/backups`             | Create backup directory in a fixed path                    |
| 3     | `mkdir -p /a/b/c/d`        | Create **parent directories recursively** if they don’t exist | `mkdir -p /var/data/app/temp`    | Ensure nested folders for config/scripts/logs exist        |
| 4     | `mkdir ./mydir`            | Create directory using **relative path** from current folder  | `mkdir ./reports`                | Create reports folder inside current directory             |
| 5     | `mkdir -v foldername`      | **Verbose mode**: shows message confirming directory creation | `mkdir -v archivelogs`           | Helpful in scripting/logging for auditing                  |
| 6     | `mkdir folder1 folder2`    | Create **multiple directories at once**                       | `mkdir logs errors archives`     | Setup multiple project folders quickly                     |
| 7     | `mkdir "$VAR"`             | Create directory using a **shell variable**                   | `mkdir "$LOG_DIR"`               | Used in shell scripts for dynamic directory creation       |
| 8     | `mkdir --mode=755 dirname` | Create a directory with **specific permissions**              | `mkdir --mode=755 secure_folder` | Set proper access control at creation (read-write-execute) |
| 9     | `mkdir --help`             | Show help and available options for `mkdir`                   | `mkdir --help`                   | Reference options when troubleshooting or scripting        |

---

## 🛠️ Real Support Use Cases:

| 💡 Task                                   | 🔧 Command Example                    | 🛠️ Why It’s Useful                                                |
| ----------------------------------------- | ------------------------------------- | ------------------------------------------------------------------ |
| Create a new log archive folder           | `mkdir /var/log/archive`              | Organize old logs before cleanup                                   |
| Prepare directory tree for app deployment | `mkdir -p /app/deploy/config/scripts` | Ensure full directory structure exists before copying config files |
| Setup multiple batch folders in one shot  | `mkdir input output processed error`  | Separate folders for data pipeline or file-based batch job         |
| Dynamic folder creation in scripts        | `mkdir "$REPORT_DIR"`                 | Automate folder creation based on date/environment                 |
| Set permissions immediately on folder     | `mkdir --mode=755 secure_logs`        | Ensure only authorized access to sensitive logs or scripts         |

---

## 🔐 Permissions Tip (Post-Creation)

You can always change permissions after creation:

```bash
mkdir reports
chmod 750 reports
```






## ✅ `rm` Command Reference Table (Support-Focused)

| 🔢 No | ✅ Command           | 💡 Explanation                                                              | 📁 Example                | 🛠️ Use Case in Support Domain                       |
| ----- | ------------------- | --------------------------------------------------------------------------- | ------------------------- | ---------------------------------------------------- |
| 1     | `rm filename`       | Delete a single file                                                        | `rm error.log`            | Remove unwanted or rotated log file                  |
| 2     | `rm file1 file2`    | Remove **multiple files**                                                   | `rm temp.txt debug.log`   | Clean up multiple unnecessary files                  |
| 3     | `rm *.log`          | Remove all files matching pattern (wildcard)                                | `rm *.log`                | Delete all log files in current directory            |
| 4     | `rm -i filename`    | Prompt for confirmation before deleting                                     | `rm -i config.sh`         | Avoid accidental deletion of important files         |
| 5     | `rm -f filename`    | Force delete — no confirmation even if file is write-protected              | `rm -f core_dump.log`     | Remove corrupted, locked, or unnecessary large files |
| 6     | `rm -r directory/`  | Delete a directory **recursively** (including all files and subdirectories) | `rm -r old_logs/`         | Remove old nested logs/archive folders               |
| 7     | `rm -rf directory/` | Forcefully delete directory and contents without prompt                     | `rm -rf /tmp/app_backup/` | Clean up unused folders quickly, but carefully       |
| 8     | `rm -v filename`    | Verbose mode: shows what's being deleted                                    | `rm -v output.txt`        | Useful in scripts/logs to track deleted files        |
| 9     | `rm -rv folder/`    | Verbose + recursive directory delete                                        | `rm -rv /data/old/`       | Confirm deletion of nested directory contents        |
| 10    | `rm --help`         | Show help for all `rm` options                                              | `rm --help`               | Learn available options, especially for scripting    |

---

## ⚠️ Safety Tips for Support Teams:

| Tip # | Description                                                                |
| ----- | -------------------------------------------------------------------------- |
| 1     | Always use `rm -i` when deleting config or scripts manually                |
| 2     | Never run `rm -rf /` — it can wipe the entire system                       |
| 3     | Double-check path when using variables in scripts with `rm`                |
| 4     | Prefer `mv` (move) to backup folder instead of deleting critical files     |
| 5     | Use `find` with `-delete` carefully and always dry run with `-print` first |

---

## 🛠️ Real Support Use Cases

| 💡 Task                                      | 🔧 Command Example                          | 🛠️ Reason                                        |
| -------------------------------------------- | ------------------------------------------- | ------------------------------------------------- |
| Clean up `.tmp` files older than a week      | `find /tmp -name "*.tmp" -mtime +7 -delete` | Keep temp folder size in check                    |
| Remove all `.log` files in backup directory  | `rm -rf /backup/logs/*.log`                 | Free up space after backing up logs to cloud/SFTP |
| Delete archived folders after ZIP transfer   | `rm -rf /app/exports/2025_*.bak/`           | Clean old exported data after verifying sent      |
| Remove specific report file after email sent | `rm /reports/jan2025-summary.csv`           | Maintain only the latest report copies            |

---

## 📌 Combine `rm` with `find` for Power Cleaning

```bash
find /var/log -name "*.log" -mtime +30 -exec rm -f {} \;
```

* Deletes all `.log` files older than 30 days in `/var/log`

---

## 🧠 Alternative Safe Practice

Instead of directly deleting:

```bash
mv critical.log /backup/deleted/
```

* Keeps logs temporarily in a safe location before full deletion.






<img width="872" height="302" alt="image" src="https://github.com/user-attachments/assets/553102b0-ae8f-4fd1-a522-5b26bca69ed7" />

