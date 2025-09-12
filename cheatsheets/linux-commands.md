# Linux Commands Cheatsheet

This cheatsheet covers essential Linux commands for **system administration, security, and troubleshooting**. It’s aimed at beginner-to-intermediate users for quick reference.

---

## File and Directory Management

| Command | Description | Example |
|---------|-------------|---------|
| `ls` | List files in a directory | `ls -lah /var/log` |
| `cd` | Change directory | `cd /etc` |
| `pwd` | Print working directory | `pwd` |
| `mkdir` | Create a directory | `mkdir /home/user/test` |
| `rmdir` | Remove empty directory | `rmdir /home/user/test` |
| `rm` | Remove files or directories | `rm file.txt` / `rm -rf folder/` |
| `cp` | Copy files/directories | `cp file1.txt file2.txt /backup/` |
| `mv` | Move or rename files | `mv file.txt /tmp/` |
| `find` | Search files | `find / -name "*.log"` |
| `locate` | Quickly find files using a database | `locate passwd` |

📖 References:  
- [GNU Coreutils](https://www.gnu.org/software/coreutils/manual/coreutils.html)  
- [Linuxize: File Management Commands](https://linuxize.com/post/linux-commands-for-files-and-directories/)

---

## File Viewing and Editing

| Command | Description | Example |
|---------|-------------|---------|
| `cat` | View file contents | `cat /etc/passwd` |
| `less` | View large files page by page | `less /var/log/syslog` |
| `head` | View first N lines | `head -n 20 /var/log/auth.log` |
| `tail` | View last N lines | `tail -f /var/log/auth.log` |
| `nano` | Simple text editor | `nano file.txt` |
| `vim` | Advanced text editor | `vim file.txt` |

📖 References:  
- [GNU nano Manual](https://www.nano-editor.org/dist/latest/nano.html)  
- [Vim Documentation](https://www.vim.org/docs.php)

---

## File Permissions and Ownership

| Command | Description | Example |
|---------|-------------|---------|
| `chmod` | Change file permissions | `chmod 644 file.txt` |
| `chown` | Change file owner | `chown user:group file.txt` |
| `chgrp` | Change group ownership | `chgrp staff file.txt` |
| `umask` | Default permissions for new files | `umask 022` |

📖 References:  
- [GNU chmod Manual](https://www.gnu.org/software/coreutils/manual/html_node/chmod-invocation.html)  
- [Linuxize: File Permissions](https://linuxize.com/post/understanding-linux-file-permissions/)

---

## System Monitoring

| Command | Description | Example |
|---------|-------------|---------|
| `top` | Real-time process monitoring | `top` |
| `htop` | Interactive process viewer | `htop` |
| `ps` | List running processes | `ps aux | grep ssh` |
| `df` | Disk space usage | `df -h` |
| `du` | Directory size | `du -sh /var/log` |
| `free` | Memory usage | `free -h` |
| `uptime` | System uptime | `uptime` |
| `who` | Logged-in users | `who` |

📖 References:  
- [Linuxize: Monitoring Commands](https://linuxize.com/post/10-linux-commands-to-monitor-system-performance/)  
- [htop Documentation](https://htop.dev/)

---

## Networking Commands

| Command | Description | Example |
|---------|-------------|---------|
| `ifconfig` | View network interfaces (deprecated) | `ifconfig -a` |
| `ip addr` | Modern interface info | `ip addr show` |
| `ping` | Test connectivity | `ping 8.8.8.8` |
| `traceroute` | Trace path to host | `traceroute google.com` |
| `netstat` | Network connections | `netstat -tulnp` |
| `ss` | Socket statistics | `ss -tuln` |
| `nmap` | Network scanning | `nmap -sS 192.168.1.0/24` |

📖 References:  
- [ip Command Manual](https://man7.org/linux/man-pages/man8/ip.8.html)  
- [Nmap Official Documentation](https://nmap.org/book/man.html)

---

## Package Management

### Debian/Ubuntu (APT)
| Command | Description |
|---------|-------------|
| `apt update` | Refresh package index |
| `apt upgrade` | Upgrade packages |
| `apt install <pkg>` | Install package |
| `apt remove <pkg>` | Remove package |
| `dpkg -l` | List installed packages |

### RedHat/CentOS/Fedora (DNF/YUM)
| Command | Description |
|---------|-------------|
| `dnf update` | Update system |
| `dnf install <pkg>` | Install package |
| `dnf remove <pkg>` | Remove package |
| `yum list installed` | List installed packages |

📖 References:  
- [APT User Guide](https://wiki.debian.org/Apt)  
- [DNF Documentation](https://dnf.readthedocs.io/en/latest/)

---

## System Security Commands

| Command | Description | Example |
|---------|-------------|---------|
| `ufw status` | Check firewall status | `sudo ufw status` |
| `ufw enable` | Enable firewall | `sudo ufw enable` |
| `iptables -L` | View iptables rules | `sudo iptables -L -v -n` |
| `fail2ban-client status` | Check Fail2ban jails | `sudo fail2ban-client status` |
| `auditctl -l` | List audit rules | `sudo auditctl -l` |

📖 References:  
- [UFW Documentation](https://help.ubuntu.com/community/UFW)  
- [Iptables HOWTO](https://www.netfilter.org/documentation/HOWTO//iptables-HOWTO.html)  
- [Linux Audit Framework](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/security_guide/sec-introduction-to-auditd)

---

## Quick Tips

- Use `man <command>` to read the manual: `man ls`  
- Use `--help` for command-specific help: `ls --help`  
- Chain commands with pipes `|` for powerful operations: `ps aux | grep ssh`  
- Redirect output: `>` (overwrite) or `>>` (append): `ls > file.txt`  

---

### References

1. [GNU Coreutils](https://www.gnu.org/software/coreutils/manual/coreutils.html)  
2. [Linuxize Linux Commands](https://linuxize.com/post/linux-commands-for-files-and-directories/)  
3. [Ubuntu UFW Guide](https://help.ubuntu.com/community/UFW)  
4. [Fail2ban Wiki](https://www.fail2ban.org/wiki/index.php/Main_Page)  
5. [Nmap Documentation](https://nmap.org/book/man.html)  
6. [Linux Auditd Documentation](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/security_guide/sec-introduction-to-auditd)  

---

