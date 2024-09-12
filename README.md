# linux-common-knowledge

# Linux Commands for Disk Usage, Users, Active Processes, and Groups

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
  

- **List all disks and partitions:**
  ```
  lsblk
  ```
  
- `du` Command (Disk Usage)
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
 
- List all running processes:
  ```
  ps
  ps -e
  ps aux`
  netstat -tulnp
  lsof
  pgrep -a .
  ```

- Dynamic real-time view of active processes:
  `top`

- Detailed interactive view of active processes:
  `htop`

- List processes with pgrep:
  `pgrep -l .`

## 4. Group-Related Commands

- List all groups in the system:
  ```
  cat /etc/group
  groups
  lslogins --groups
  ```

- Show only group names:
  `cut -d: -f1 /etc/group`

- Get all groups using getent:
  `getent group`

- Show groups for a specific user:
  `groups username`

- Using awk to list groups:
  `awk -F: '{print $1}' /etc/group`

  
