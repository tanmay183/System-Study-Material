
## ✅ **What is UNIX?**

* A **multi-user**, **multi-tasking** operating system.
* Stable, secure, and widely used in **servers**, especially in **banking/finance**.
* Popular flavors: **AIX (IBM)**, **HP-UX**, **Solaris (Oracle)**, **Linux** (UNIX-like).

---

## ✅ **Why UNIX in Banking Projects?**

* **High availability** and **reliability**.
* Secure environment for sensitive transactions.
* Commonly used for hosting **core banking apps**, **batch jobs**, **middleware**, and **database servers**.

---

## ✅ **Basic UNIX Structure**

* **Kernel** – Core of the OS.
* **Shell** – Interface to run commands (`bash`, `ksh`, `sh`).
* **File System** – Hierarchical structure starting from `/` (root).

---

## ✅ **Common Directories**

| Directory       | Purpose                      |
| --------------- | ---------------------------- |
| `/home`         | User files                   |
| `/var`          | Variable data (logs, spools) |
| `/etc`          | Configuration files          |
| `/tmp`          | Temporary files              |
| `/bin`, `/sbin` | Essential commands           |

---

## ✅ **Important UNIX Commands**

| Task                   | Command Example                     |
| ---------------------- | ----------------------------------- |
| List files             | `ls -l`, `ls -a`                    |
| View file content      | `cat`, `more`, `less`, `tail -f`    |
| Copy/Move/Delete files | `cp`, `mv`, `rm`                    |
| Edit file              | `vi`, `nano`                        |
| Process monitoring     | `ps -ef`, `top`, `kill PID`         |
| Disk usage             | `df -h`, `du -sh`                   |
| Search logs            | `grep "ERROR" app.log`              |
| Schedule jobs          | `crontab -l`, `crontab -e`          |
| Permissions            | `chmod`, `chown`, `ls -l`           |
| Network check          | `ping`, `netstat`, `telnet`, `curl` |
| View system uptime     | `uptime`, `who`, `w`                |

---

## ✅ **File Permissions**

```
-rwxr-xr-- 1 user group  size date file.sh
```

* **Owner/Group/Others**: `r` (read), `w` (write), `x` (execute)
* Use `chmod 755 file.sh` to set permissions

---

## ✅ **Useful Tools**

| Tool      | Use Case            |
| --------- | ------------------- |
| `vi`      | Edit files          |
| `tail -f` | Live log monitoring |
| `cron`    | Job scheduling      |
| `ssh`     | Remote access       |

---

## ✅ **Support-Relevant Use Cases**

| Issue              | UNIX Task                    |                     |
| ------------------ | ---------------------------- | ------------------- |
| App not responding | \`ps -ef                     | grep app\`, restart |
| Logs needed        | `cd /var/log`, `grep` errors |                     |
| Disk full          | `df -h`, clear old logs      |                     |
| Job failed         | Check `crontab`, script logs |                     |
| Permission denied  | `chmod`, `chown`             |                     |

