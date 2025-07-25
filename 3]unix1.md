## ✅ `ls` Command Master Table (Complete)

| 🔢 No | ✅ Command Option               | 💡 Explanation                                           | 📁 Example                        | 🛠️ Use Case in Support Domain                            |
| ----- | ------------------------------ | -------------------------------------------------------- | --------------------------------- | --------------------------------------------------------- |
| 1     | `ls`                           | List files and directories in current directory          | `ls`                              | Check directory contents                                  |
| 2     | `ls -l`                        | Long listing: shows permissions, owner, size, date, etc. | `ls -l`                           | View file metadata, useful in RCA                         |
| 3     | `ls -a`                        | Show hidden files (starting with `.`)                    | `ls -a`                           | See hidden config like `.env`, `.bashrc`                  |
| 4     | `ls -la` / `ls -al`            | Long listing + show hidden files                         | `ls -la`                          | Check permissions of hidden files                         |
| 5     | `ls -lh`                       | Long listing with human-readable file sizes              | `ls -lh`                          | Quickly see file sizes in KB, MB, GB                      |
| 6     | `ls -ltr`                      | Sort by modified time (oldest first), long listing       | `ls -ltr`                         | See execution history of batch jobs/logs                  |
| 7     | `ls -lt`                       | Sort by modified time (newest first)                     | `ls -lt`                          | Find the latest logs or modified files                    |
| 8     | `ls -lS`                       | Sort by file size (largest first)                        | `ls -lS`                          | Identify which logs are consuming most disk               |
| 9     | `ls -lhS`                      | Sort by size + human-readable format                     | `ls -lhS`                         | Find large log or dump files                              |
| 10    | `ls -R`                        | List contents recursively in all subdirectories          | `ls -R /var/log`                  | Explore nested log/config directories                     |
| 11    | `ls -d */`                     | List only directories                                    | `ls -d */`                        | Get a clean list of folders (e.g., environments, backups) |
| 12    | `ls -1`                        | One entry per line (good for scripts)                    | `ls -1`                           | Useful in automation or looping through files             |
| 13    | `ls -F`                        | Append `/` for dirs, `*` for executables                 | `ls -F`                           | Identify file types visually                              |
| 14    | `ls -i`                        | Display inode number                                     | `ls -i`                           | Troubleshoot filesystem/link issues                       |
| 15    | `ls -r`                        | Reverse order while sorting                              | `ls -ltr` → `ls -ltr -r`          | View logs or backups in reverse order                     |
| 16    | `ls -t`                        | Sort by time (newest to oldest)                          | `ls -lt`                          | Locate the latest updated file/log                        |
| 17    | `ls -X`                        | Sort by file extension                                   | `ls -lX`                          | Group files by type (e.g., `.log`, `.sh`, `.csv`)         |
| 18    | `ls --color=auto`              | Colored output (if supported)                            | `ls --color=auto`                 | Easier to distinguish dirs/files in SSH                   |
| 19    | `ls *log`                      | Search files by pattern (glob matching)                  | `ls *log`                         | List all log files in directory                           |
| 20    | `ls *.sh`                      | Show only shell scripts                                  | `ls *.sh`                         | Locate maintenance/cron shell scripts                     |
| 21    | `ls *2025*`                    | List files containing "2025" in name                     | `ls *2025*`                       | Locate logs or files for a specific year                  |
| 22    | `ls -p`                        | Append `/` to directories                                | `ls -p`                           | Easy visual way to spot folders                           |
| 23    | `ls -Q`                        | Enclose file names in double quotes                      | `ls -Q`                           | Useful when filenames contain spaces                      |
| 24    | `ls -v`                        | Natural version sort (1, 2, ..., 10 instead of 1, 10, 2) | `ls -v`                           | Sort logs with versioned names properly                   |
| 25    | `ls --sort=extension`          | Sort files by extension                                  | `ls --sort=extension`             | Helpful to see `.log`, `.csv`, `.conf` separately         |
| 26    | `ls --group-directories-first` | List folders before files                                | `ls --group-directories-first -l` | Makes directory navigation clearer                        |
| 27    | `ls -Z`                        | Show SELinux context (if enabled)                        | `ls -Z`                           | Used in secure environments (Red Hat, Banking Infra)      |
| 28    | `ls -c`                        | Sort by change time (not modify time)                    | `ls -lc`                          | Detect configuration or permission changes                |
| 29    | `ls -u`                        | Sort by access time                                      | `ls -lu`                          | Debug who/when last accessed a file                       |

---

## 📦 Bonus: Combine `ls` with Other Commands

| 💡 Task                               | 🔧 Command Example                            | 🛠️ Use Case                                   |                                                 |
| ------------------------------------- | --------------------------------------------- | ---------------------------------------------- | ----------------------------------------------- |
| Show latest 5 logs                    | \`ls -lt \*.log                               | head -5\`                                      | Quickly locate recent log activity              |
| Count number of `.log` files          | \`ls \*.log                                   | wc -l\`                                        | Check if expected number of log files generated |
| View total disk usage by `.log` files | `du -sh *.log`                                | See how much space logs are consuming          |                                                 |
| List only files (no dirs)             | \`ls -p                                       | grep -v /\`                                    | Filter out directories                          |
| View files modified in last 1 day     | `find . -type f -mtime -1 -exec ls -lh {} \;` | Incident investigation or job failure analysis |                                                 |
| Search files with `ERROR` in name     | \`ls                                          | grep ERROR\`                                   | Debugging failed/error-based log files          |

---

## 🧠 Pro Tip for Support Teams:

Create aliases for frequent `ls` uses in `.bashrc`:

```bash
alias ll='ls -lh'
alias ltr='ls -ltr'
alias lt='ls -lt'
alias la='ls -la'
```

Then reload:

```bash
source ~/.bashrc
```



### file start with :
- i.e dash = it means file   d = it means directory   l = means link


### Every Linux system have three types of owner:
   - User: A user is the one who created the file. By default, whosoever, creates the file becomes the owner of the file. A user can create, delete, or modify the file.
   - Group: A group can contain multiple users. All the users belonging to a group have same access permission for a file.
   - Other: Any one who has access to the file other than user and group comes in the category of other. Other has neither created the file nor is a group member.

### Users and groups can be locally managed in /etc/psswd or /etc/group.

r-read       w-write        x-execute

Each permission (r, w, x) has a corresponding octal value: r = 4, w = 2, and x = 1.
