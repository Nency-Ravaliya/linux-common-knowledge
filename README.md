# linux-common-knowledge

# Linux Commands for Disk Usage, Users, Active Processes, and Groups, Blocks, CPU utilization

## 1. Disk Usage Commands

- **Check disk space usage**:
  ```bash
  df -h
  df
  ```

- **Check free and used memory**:
  ```
  free -h
  free
  free -m
  free -g
  ```
  

- **List all disks and partitions**:
  ```
  lsblk
  ```
  
- **`du` Command (Disk Usage)**:
  ```
  du
  du -h
  du -sh /home
  cat /proc/partitions
  ls /dev/disk/by-id/
  sudo hwinfo --disk
  ```

- **Detailed information on storage devices**:
  ` sudo fdisk -l`

## 2. User-Related Commands
  
- **List all users in the system**:
    `cat /etc/passwd`

- **Get a list of logged-in users**:
  ```
  who
  w
  compgen -u
  users
  lslogins
  lslogins -u
  getent passwd
  ```

 ## 3. Active Process Commands
 
- **List all running processes**:
  ```
  ps
  ps -e
  ps aux`
  netstat -tulnp
  lsof
  pgrep -a .
  ```

- **Dynamic real-time view of active processes**:
  `top`

- **Detailed interactive view of active processes**:
  `htop`

- **List processes with pgrep**:
  `pgrep -l .`

## 4. Group-Related Commands

- **List all groups in the system**:
  ```
  cat /etc/group
  groups
  lslogins --groups
  ```

- **Show only group names**:
  `cut -d: -f1 /etc/group`

- **Get all groups using `getent`**:
  `getent group`

- **Show groups for a specific user**:
  `groups username`

- **Using awk to list groups**:
  `awk -F: '{print $1}' /etc/group`

 ## 5. CPU Utilization Commands
 
1. **`top`**
   - Real-time CPU and system performance monitor.
   - **Command:**
     ```bash
     top
     ```

2. **`htop`**
   - Interactive process viewer with CPU usage (requires installation).
   - **Command:**
     ```bash
     htop
     ```
   - **Installation (if not installed):**
     ```bash
     sudo apt install htop
     ```

3. **`mpstat`**
   - Displays CPU usage statistics per core (part of `sysstat` package).
   - **Command:**
     ```bash
     mpstat
     ```
   - **Installation (if not installed):**
     ```bash
     sudo apt install sysstat
     ```

4. **`iostat`**
   - Reports CPU and I/O statistics (part of `sysstat` package).
   - **Command:**
     ```bash
     iostat
     ```
   - **Installation (if not installed):**
     ```bash
     sudo apt install sysstat
     ```

5. **`sar`**
   - Provides historical CPU usage statistics (part of `sysstat` package).
   - **Command:**
     ```bash
     sar -u 1 3
     ```
   - **Installation (if not installed):**
     ```bash
     sudo apt install sysstat
     ```

6. **`vmstat`**
   - Shows CPU, memory, and system statistics.
   - **Command:**
     ```bash
     vmstat 1 5
     ```

7. **`uptime`**
   - Displays system load averages over the past 1, 5, and 15 minutes.
   - **Command:**
     ```bash
     uptime
     ```

8. **`ps`**
   - Shows CPU usage by individual processes.
   - **Command:**
     ```bash
     ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%cpu
     ```

9. **`pidstat`**
   - CPU usage statistics for individual processes (part of `sysstat` package).
   - **Command:**
     ```bash
     pidstat
     ```
   - **Installation (if not installed):**
     ```bash
     sudo apt install sysstat
     ```

10. **`nmon`**
    - Real-time CPU and system performance monitor (requires installation).
    - **Command:**
      ```bash
      nmon
      ```
    - **Installation (if not installed):**
      ```bash
      sudo apt install nmon
      ```

11. **`dstat`**
    - Combines CPU, disk, and network statistics (requires installation).
    - **Command:**
      ```bash
      dstat
      ```
    - **Installation (if not installed):**
      ```bash
      sudo apt install dstat
      ```
