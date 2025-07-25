
## ✅ **1. OS Fundamentals**

**Why it matters:** You need to understand how the system works to troubleshoot issues related to resources, processes, memory, or system performance.

### Key Topics:

* **What is an Operating System?**

  * Interface between user and hardware.
  * Manages processes, memory, file systems, I/O, and hardware devices.

* **Types of OS**

  * **Windows, Linux/Unix** – Common in banking servers.
  * **Difference between GUI & CLI-based OS**

---

## ✅ **2. Common OS Used in Banking**

* **Linux/Unix** – Preferred for backend services, core banking apps.
* **Windows Server** – Used for middleware apps, batch jobs, desktop tools.

> 🔴 *You must know how to work in Linux terminal and Windows command line.*

---

## ✅ **3. Linux/Unix Commands (Most Important for Support Role)**

### 🔧 Basic File Operations:

| Command               | Description                          |
| --------------------- | ------------------------------------ |
| `ls`, `cd`, `pwd`     | List, navigate, print directory path |
| `cp`, `mv`, `rm`      | Copy, move, delete files/folders     |
| `cat`, `more`, `less` | Read file contents                   |
| `vi`, `nano`          | Edit files in CLI                    |

### 🔍 Process & Resource Monitoring:

| Command                 | Description             |
| ----------------------- | ----------------------- |
| `ps -ef`, `top`, `htop` | Check running processes |
| `kill`, `kill -9`       | Kill a process          |
| `df -h`, `du -sh`       | Disk usage and space    |
| `free -m`, `vmstat`     | Check memory usage      |

### 📂 Logs and Troubleshooting:

| Command              | Description                         |
| -------------------- | ----------------------------------- |
| `tail -f`, `grep`    | Real-time log monitoring, filtering |
| `dmesg`              | View kernel messages                |
| `journalctl`         | System logs (systemd-based OS)      |
| `who`, `w`, `uptime` | User login and system status        |

> 🟢 *Must be comfortable with checking logs in `/var/log`, for ex: `tail -f /var/log/messages`*

---

## ✅ **4. User & Permission Management**

* `chmod`, `chown`, `chgrp` – File permission handling
* `useradd`, `passwd`, `usermod` – User management
* `sudo`, `su` – Privilege elevation

---

## ✅ **5. Crontab (Scheduled Jobs)**

* Used for scheduling scripts/batch jobs (e.g., report generation).

```bash
crontab -e         # Edit cron jobs
crontab -l         # List current cron jobs
```

Example:

```
0 2 * * * /home/user/scripts/batch.sh > /tmp/batch.log 2>&1
```

---

## ✅ **6. Networking Basics in OS**

* Check connectivity: `ping`, `traceroute`, `telnet`, `netstat`, `curl`, `nslookup`
* Ports: Know how to identify listening ports (`netstat -tuln`, `ss -tuln`)
* DNS Issues: `dig`, `host`, `nslookup`

> 🔄 *Important for resolving app connectivity issues, API failures, DB connection errors*

---

## ✅ **7. Shell Scripting (Must-Have for Automation)**

* Basics of `bash` scripting: variables, loops, if-else
* Writing a health check or log rotation script
* Parameterized scripts for cron jobs

Example: Simple log search script

```bash
#!/bin/bash
grep "ERROR" /var/log/app.log > error_report.txt
```

---

## ✅ **8. System Monitoring Tools (GUI/CLI)**

* Linux CLI: `top`, `htop`, `iotop`, `nmon`
* Windows: Task Manager, Resource Monitor
* Bank-specific: Tools like **Nagios**, **AppDynamics**, **Zabbix**, **Grafana**, etc.

---

## ✅ **9. File Systems & Mounting**

* Check disk partitions: `lsblk`, `df -h`
* Mount/unmount: `mount`, `umount`
* Understand `/etc/fstab` and auto-mounting issues

---

## ✅ **10. Backup & Recovery Basics**

* File compression: `tar`, `gzip`, `zip`
* Backup scripts: Periodic file dumps
* Snapshot handling (VM or Database backups)

---

## ✅ **11. Incident Handling & RCA**

* How to collect logs, system info during incident
* Basic checklist:

  * Is the app running?
  * Is the port open?
  * Any error in logs?
  * Disk full?
  * User permissions?
  * DB connectivity?

---

## ✅ **12. Windows-Specific Knowledge**

* Services management: `services.msc`, `net start/stop`
* Task Scheduler for batch jobs
* `Event Viewer` for logs
* CMD / PowerShell basics

---

## ✅ **13. Application Support Scenarios (Common)**

| Problem                       | OS Commands/Actions                            |
| ----------------------------- | ---------------------------------------------- |
| Application not running       | `ps`, check logs, restart service              |
| App crashes due to disk space | `df -h`, clear `/tmp`, logs                    |
| DB Connection timeout         | `ping`, `telnet`, firewall check               |
| Scheduled job not working     | `crontab -l`, check script permission and logs |
| High CPU/memory usage         | `top`, `kill`, app log trace                   |

---

## ✅ **14. Tools to Learn**

| Tool                | Purpose                      |
| ------------------- | ---------------------------- |
| **Putty/MobaXterm** | SSH into Linux systems       |
| **WinSCP**          | Transfer files securely      |
| **Notepad++**       | Log reading, file editing    |
| **JIRA/SNOW**       | Ticketing & issue tracking   |
| **Git**             | (If version control is used) |

---

## ✅ **15. Real-World Tips**

* Always take a backup before modifying anything
* Document the incident and resolution (important in banking)
* Know your escalation matrix and SLAs
* Learn how to write KB (Knowledge Base) articles

---


