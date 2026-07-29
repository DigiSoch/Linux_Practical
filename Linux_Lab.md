# Linux_Practical
It cover all basic and advance commands and their result

>##### To check current username


`username@hostname:~$ whoami`

arvind

>##### To check all user login info

`username@hostname:~$ w`

```bash
 09:55:38 up 22 min,  1 user,  load average: 0.02, 0.01, 0.00
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU  WHAT
arvind   pts/1    -                09:33   22:18   0.07s  0.06s -bash

```
>[!NOTE]
**Understanding the Columns of w:**
>**USER:** The username of the logged-in individual.
>
>**TTY:** The terminal type being used.
>
>**ttyX (e.g., tty1)**: A physical or native Virtual bash terminal directly on the machine.
>
>**pts/X (e.g., pts/1)**: A Pseudo-Terminal Slave (emulated terminal used via GUI terminal applications or SSH/Telnet).
>
>**FROM:** The source hostname or IP address the user is connecting from (blank or :0 means local).
>
>**LOGIN@:** The exact time the session was initiated.
>
>**IDLE:** The duration since the user last entered a command into that specific terminal. Resets to 0.00s when Enter is pressed.
>
>**JCPU (Joint CPU):** Total CPU time used by all processes attached to that TTY since login.
>
>**PCPU (Process CPU):** CPU time used specifically by the currently active process listed in the WHAT column.
>
>**WHAT:** The current command or process actively running (defaults to the shell, e.g., -bash).
>

>##### List files, directories

```bash
username@hostname:~$ ls



a32.sh  abc.txt  arvindTest  automated_youtube_channel  bash_test.sh  
linux_basic_commands.txt
```
>##### Long list files, directories with permission, size, type, timestamp, user, group

```bash
username@hostname:~$ ls -lrt

total 28
drwx------ 3 arvind arvind 4096 Feb  2  2025 snap

drwxr-xr-x 3 arvind arvind 4096 Apr 19  2025 arvindTest
-rwxr-xr-x 1 arvind arvind   58 Jul  6 05:12 a32.sh
-rwxr-xr-x 1 arvind arvind   98 Jul  6 06:48 bash_test.sh
-rw-r--r-- 1 arvind arvind   20 Jul  6 06:52 abc.txt
-rw-r--r-- 1 arvind arvind 4096 Jul  7 10:14 linux_basic_commands.txt
```

>##### list all files folder inclusing hidden
```bash
username@hostname:~$ ls -la

total 96
drwxr-x--- 10 arvind arvind  4096 Jul  7 09:55 .
drwxr-xr-x  3 root   root    4096 Jan 22  2025 ..
-rw-------  1 arvind arvind 10030 Jul  6 07:12 .bash_history
-rw-r--r--  1 arvind arvind   220 Jan 22  2025 .bash_logout
-rw-r--r--  1 arvind arvind  3809 Jan 22  2025 .bashrc
drwx------  4 arvind arvind  4096 Feb  2  2025 .cache
drwxr-xr-x  6 arvind arvind  4096 Feb 16  2025 .config
drwxr-xr-x  2 arvind arvind  4096 Jan 22  2025 .landscape
-rw-------  1 arvind arvind    47 Jul  6 06:52 .lesshst
drwxr-xr-x  3 arvind arvind  4096 Jan 22  2025 .local
-rw-r--r--  1 arvind arvind     0 Jul  7 09:33 .motd_shown
-rw-r--r--  1 arvind arvind   807 Jan 22  2025 .profile
-rw-------  1 arvind arvind   119 Feb 19  2025 .python_history
-rw-r--r--  1 arvind arvind    66 Mar  7  2025 .selected_editor
drwx------  2 arvind arvind  4096 Feb 19  2025 .ssh
-rw-r--r--  1 arvind arvind     0 Jan 23  2025 .sudo_as_admin_successful
-rw-------  1 arvind arvind  1377 Jul  6 05:00 .viminfo
-rwxr-xr-x  1 arvind arvind    58 Jul  6 05:12 a32.sh
-rw-r--r--  1 arvind arvind    20 Jul  6 06:52 abc.txt
drwxr-xr-x  3 arvind arvind  4096 Apr 19  2025 arvindTest
```
>**ls -la show all files including hidden files/folders**

>[!NOTE]
> here l long list, r revers order, t time

```bash
username@hostname:~$ ls -lrth

total 32K
drwx------ 3 arvind arvind 4.0K Feb  2  2025 snap
drwxr-xr-x 3 arvind arvind 4.0K Feb 19  2025 automated_youtube_channel
drwxr-xr-x 3 arvind arvind 4.0K Apr 19  2025 arvindTest
-rwxr-xr-x 1 arvind arvind   58 Jul  6 05:12 a32.sh
-rwxr-xr-x 1 arvind arvind   98 Jul  6 06:48 bash_test.sh
-rw-r--r-- 1 arvind arvind   20 Jul  6 06:52 abc.txt
-rw-r--r-- 1 arvind arvind 8.0K Jul  7 10:16 linux_basic_commands.txt
```
```bash
username@hostname:~$ pwd

/home/arvind
```
```bash
username@hostname:~$ touch avg.txt

username@hostname:~$ mkdir kumar doucment
```

```bash
username@hostname:~$ ls -lrt

total 40
drwx------ 3 arvind arvind 4096 Feb  2  2025 snap

drwxr-xr-x 3 arvind arvind 4096 Apr 19  2025 arvindTest
-rwxr-xr-x 1 arvind arvind   58 Jul  6 05:12 a32.sh
-rwxr-xr-x 1 arvind arvind   98 Jul  6 06:48 bash_test.sh
-rw-r--r-- 1 arvind arvind   20 Jul  6 06:52 abc.txt
-rw-r--r-- 1 arvind arvind 8192 Jul  7 10:16 linux_basic_commands.txt
-rw-r--r-- 1 arvind arvind    0 Jul  7 10:19 avg.txt
drwxr-xr-x 2 arvind arvind 4096 Jul  7 10:20 kumar
drwxr-xr-x 2 arvind arvind 4096 Jul  7 10:20 doucment
```
```bash
username@hostname:~$ ls -lrt doucment

total 0
username@hostname:~$ mkdir -p project1/fortend
```

```bash
username@hostname:~$ ls -lrt

total 44
drwx------ 3 arvind arvind 4096 Feb  2  2025 snap

drwxr-xr-x 3 arvind arvind 4096 Apr 19  2025 arvindTest
-rwxr-xr-x 1 arvind arvind   58 Jul  6 05:12 a32.sh
-rwxr-xr-x 1 arvind arvind   98 Jul  6 06:48 bash_test.sh
-rw-r--r-- 1 arvind arvind   20 Jul  6 06:52 abc.txt
-rw-r--r-- 1 arvind arvind 8192 Jul  7 10:16 linux_basic_commands.txt
-rw-r--r-- 1 arvind arvind    0 Jul  7 10:19 avg.txt
drwxr-xr-x 2 arvind arvind 4096 Jul  7 10:20 kumar
drwxr-xr-x 2 arvind arvind 4096 Jul  7 10:20 doucment
drwxr-xr-x 3 arvind arvind 4096 Jul  7 10:23 project1
```
```bash
username@hostname:~$ ls -lrt project1

total 4
drwxr-xr-x 2 arvind arvind 4096 Jul  7 10:23 fortend
```
> total 4 This indicates the total disk space allocated for all files in this directory, measured in blocks (usually 4KB per block).       

```bash
username@hostname:~$    ls -lrta project1

total 12
drwxr-xr-x  2 arvind arvind 4096 Jul  7 10:23 fortend
drwxr-x--- 13 arvind arvind 4096 Jul  7 10:23 ..
drwxr-xr-x  3 arvind arvind 4096 Jul  7 10:23 .
```

```bash
username@hostname:~$ : << 'EOF'

d rwxr-xr-x   2   arvind   arvind   4096   Jul 7 10:23   fortend

 └────┬────┘  ─┬─  ───┬──   ───┬──   ──┬─   ──────┬─────   ───┬───
      │        │      │        │       │          │           └─ File/Directory Name
      │        │      │        │       │          └─ Last Modified Date & Time
      │        │      │        │       └─ Size in Bytes (4096 bytes)
      │        │      └─ User Owner (Creator)
      │        └─ Number of Hard Links
      └─ File Type & Permissions
     
```
 
```bash
username@hostname:~$ :
```
>**The command : don't do any task**

```bash
username@hostname:~$ apt --version

apt 2.7.14 (amd64)
```

> a**pt is package manager use for install, update, upgrade,remove packages**


```bash
username@hostname:~$ df -kh

Filesystem      Size  Used Avail Use% Mounted on
none            3.7G     0  3.7G   0% /usr/lib/modules/6.18.33.2-microsoft-standard-WSL2
none            3.7G  4.0K  3.7G   1% /mnt/wsl
drivers         359G  187G  172G  53% /usr/lib/wsl/drivers
/dev/sdd        251G  3.9G  235G   2% /
none            3.7G   40K  3.7G   1% /mnt/wslg
none            3.7G     0  3.7G   0% /usr/lib/wsl/lib
rootfs          3.7G  2.8M  3.7G   1% /init
none            3.7G  828K  3.7G   1% /run
none            3.7G     0  3.7G   0% /run/lock
none            3.7G     0  3.7G   0% /run/shm
none            3.7G  104K  3.7G   1% /mnt/wslg/versions.txt
none            3.7G  104K  3.7G   1% /mnt/wslg/doc
C:\             359G  187G  172G  53% /mnt/c
D:\             118G   22G   97G  19% /mnt/d
snapfuse         67M   67M     0 100% /snap/core24/1587
snapfuse         67M   67M     0 100% /snap/core24/1643
snapfuse         50M   50M     0 100% /snap/snapd/26865
snapfuse        128K  128K     0 100% /snap/tldr/666
snapfuse        128K  128K     0 100% /snap/tldr/791
tmpfs           754M   20K  754M   1% /run/user/1000
snapfuse         51M   51M     0 100% /snap/snapd/27406
```
```bash
username@hostname:~$ ls

a32.sh  abc.txt  arvindTest  automated_youtube_channel  avg.txt  bash_test.sh  doucment  kumar  linux_basic_commands.txt  project1  snap
```
```bash
username@hostname:~$ cd project1

username@hostname:~/project1$ cd ..

username@hostname:~$ cd project1/fortend/

username@hostname:~/project1/fortend$ cd ~

username@hostname:~$ cd /
21
username@hostname:/$ pwd

/
username@hostname:/$ cd /etc

username@hostname:/etc$ cd

username@hostname:~$ finger

Command 'finger' not found, but can be installed with:
sudo apt install finger
```
```bash
username@hostname:~$ who

arvind   pts/1        2026-07-07 09:33
```


```bash
username@hostname:~$ free

              total        used        free      shared  buff/cache   available
Mem:         7719564      594508     7006348        3912      272392     7125056
Swap:        2097152           0     2097152

```
```bash
username@hostname:~$ free -h

               total        used        free      shared  buff/cache   available
Mem:           7.4Gi       580Mi       6.7Gi       3.8Mi       266Mi       6.8Gi
Swap:          2.0Gi          0B       2.0Gi

```

**This command use to check memory of system**


```bash
username@hostname:~$ pwd

/home/arvind
username@hostname:~$       ls

a32.sh  abc.txt  arvindTest  automated_youtube_channel  avg.txt  bash_test.sh  doucment  kumar  linux_basic_commands.txt  project1  snap

username@hostname:~$  cd /

username@hostname:/$ ls -ls

total 2868
   0 lrwxrwxrwx   1 root root       7 Apr 22  2024 bin -> usr/bin
   4 drwxr-xr-x   2 root root    4096 Feb 26  2024 bin.usr-is-merged
   4 drwxr-xr-x   2 root root    4096 Apr 22  2024 boot
   0 drwxr-xr-x  15 root root    3860 Jul  7 09:33 dev
   4 drwxr-xr-x  98 root root    4096 Jul  7 10:35 etc
   4 drwxr-xr-x   3 root root    4096 Jan 22  2025 home
2772 -rwxr-xr-x   1 root root 2836528 Jun 25 21:27 init
   0 lrwxrwxrwx   1 root root       7 Apr 22  2024 lib -> usr/lib
   4 drwxr-xr-x   2 root root    4096 Apr  8  2024 lib.usr-is-merged
   0 lrwxrwxrwx   1 root root       9 Apr 22  2024 lib64 -> usr/lib64
  16 drwx------   2 root root   16384 Apr 10  2019 lost+found
   4 drwxr-xr-x   2 root root    4096 Jan  6  2025 media
   4 drwxr-xr-x   6 root root    4096 Jan 23  2025 mnt
   4 drwxr-xr-x   2 root root    4096 Jan  6  2025 opt
   0 dr-xr-xr-x 264 root root       0 Jul  7 09:33 proc
   4 drwx------   3 root root    4096 Jan 23  2025 root
   0 drwxr-xr-x  19 root root     560 Jul  7 09:33 run
   0 lrwxrwxrwx   1 root root       8 Apr 22  2024 sbin -> usr/sbin
   4 drwxr-xr-x   2 root root    4096 Mar 31  2024 sbin.usr-is-merged
   4 drwxr-xr-x   6 root root    4096 Feb  2  2025 snap
   4 drwxr-xr-x   2 root root    4096 Jan  6  2025 srv
   0 dr-xr-xr-x  13 root root       0 Jul  7 11:20 sys
   4 drwxrwxrwt   8 root root    4096 Jul  7 09:39 tmp
   4 drwxr-xr-x  12 root root    4096 Jan  6  2025 usr
   4 drwxr-xr-x  13 root root    4096 Jan 23  2025 var
   4 drwx------   2 root root    4096 Jan 29  2025 wslECImHn
   4 drwx------   2 root root    4096 Jan 29  2025 wslMAggHn
   4 drwx------   2 root root    4096 Jan 29  2025 wslNNnCDn
   4 drwx------   2 root root    4096 Jan 29  2025 wsldEDMFn
   4 drwx------   2 root root    4096 Jan 29  2025 wslocADIn
```
```bash
username@hostname:/$ pwd

/
```

##### To get information about the current process and system information like current RAM usage, CPU usage, etc.


```bash
username@hostname:~$ cd /proc/

username@hostname:/proc$ ls -lrt

total 0
lrwxrwxrwx  1 root             root                           0 Jul  7 09:33 thread-self -> 1745/task/1745
lrwxrwxrwx  1 root             root                           0 Jul  7 09:33 self -> 1745
dr-xr-xr-x  1 root             root                           0 Jul  7 09:33 sys
-r--r--r--  1 root             root                         146 Jul  7 09:33 cmdline
lrwxrwxrwx  1 root             root                          11 Jul  7 09:33 mounts -> self/mounts
-r--r--r--  1 root             root                           0 Jul  7 09:33 filesystems
dr-xr-xr-x  9 root             root                           0 Jul  7 09:33 2
dr-xr-xr-x  9 root             root                           0 Jul  7 09:33 1
lrwxrwxrwx  1 root             root                           8 Jul  7 09:33 net -> self/net
-r--------  1 root             root             140737471594496 Jul  7 09:33 kcore
-r--r--r--  1 root             root                           0 Jul  7 09:33 cpuinfo
dr-xr-xr-x  5 root             root                           0 Jul  7 09:33 pressure
dr-xr-xr-x  9 root             root                           0 Jul  7 09:33 7
-r--r--r--  1 root             root                           0 Jul  7 09:33 uptime
-r--r--r--  1 root             root                           0 Jul  7 09:33 swaps
-r--r--r--  1 root             root                           0 Jul  7 09:33 devices
dr-xr-xr-x  9 root             root                           0 Jul  7 09:33 56
-r--r--r--  1 root             root                           0 Jul  7 09:33 meminfo
```
```bash
username@hostname:/proc$ cat meminfo

MemTotal:        7719564 kB
MemFree:         7004168 kB
MemAvailable:    7123684 kB
Buffers:            6652 kB
Cached:           244492 kB
SwapCached:            0 kB
Active:            79352 kB
Inactive:         309124 kB
Active(anon):       2612 kB
Inactive(anon):   138656 kB
Active(file):      76740 kB
Inactive(file):   170468 kB
Unevictable:           0 kB
Mlocked:               0 kB
SwapTotal:       2097152 kB
SwapFree:        2097152 kB
Dirty:                20 kB
Writeback:             0 kB
AnonPages:        137544 kB
Mapped:           154092 kB
Shmem:              3916 kB
KReclaimable:      22064 kB
```

```bash
username@hostname:~$ cat /proc/cpuinfo

processor       : 0
vendor_id       : AuthenticAMD
cpu family      : 25
model           : 68
model name      : AMD Ryzen 5 7535HS with Radeon Graphics
stepping        : 1
microcode       : 0xffffffff
cpu MHz         : 3293.722
cache size      : 512 KB
physical id     : 0
siblings        : 12
core id         : 0
cpu cores       : 6
apicid          : 0
initial apicid  : 0
fpu             : yes
fpu_exception   : yes
cpuid level     : 13
wp              : yes

```
```bash

username@hostname:~$ cat /etc/*release

DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=24.04
DISTRIB_CODENAME=noble
DISTRIB_DESCRIPTION="Ubuntu 24.04.2 LTS"
PRETTY_NAME="Ubuntu 24.04.2 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.2 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo

```

##### apropos command search the short discription for the give command , and command name. 

1. Run if the below command giving error not appripate
`sudo mandb`

```
bob@ubuntu-host ~ ➜  apropos ssh
authorized_keys (5)  - OpenSSH daemon
EVP_KDF-SSHKDF (7ssl) - The SSHKDF EVP_KDF implementation
git-shell (1)        - Restricted login shell for Git-only SSH access
rcp (1)              - OpenSSH secure file copy
rlogin (1)           - OpenSSH remote login client
rsh (1)              - OpenSSH remote login client
scp (1)              - OpenSSH secure file copy
sftp (1)             - OpenSSH secure file transfer
sftp-server (8)      - OpenSSH SFTP server subsystem
slogin (1)           - OpenSSH remote login client
ssh (1)              - OpenSSH remote login client
ssh-add (1)          - adds private key identities to the OpenSSH authentication agent
ssh-agent (1)        - OpenSSH authentication agent
ssh-argv0 (1)        - replaces the old ssh command-name as hostname handling
ssh-copy-id (1)      - use locally available keys to authorise logins on a remote machine
ssh-keygen (1)       - OpenSSH authentication key utility
ssh-keyscan (1)      - gather SSH public keys from servers
ssh-keysign (8)      - OpenSSH helper for host-based authentication
ssh-pkcs11-helper (8) - OpenSSH helper for PKCS#11 support
ssh-sk-helper (8)    - OpenSSH helper for FIDO authenticator support
ssh_config (5)       - OpenSSH client configuration file
sshd (5)             - OpenSSH daemon
sshd (8)             - OpenSSH daemon
sshd_config (5)      - OpenSSH daemon configuration file
sshpass (1)          - noninteractive ssh password provider
```
##### hstnamectl command for manage hostname like , changing hostname
EX - 

`sudo hostnamectl --static hostname arvind-host`

```bash
username@hostname:~$ uptime

 11:48:13 up  2:15,  1 user,  load average: 0.05, 0.01, 0.00
```

##### show last login history of user

`last` command is used to show the for last 30 days of login history for the current user.

```bash

username@hostname:~$ last

reboot   system boot  6.18.33.2-micros Tue Jul  7 09:33   still running
reboot   system boot  6.18.33.2-micros Mon Jul  6 04:55 - 08:29 (1+03:34)
reboot   system boot  6.18.33.2-micros Sun Jul  5 18:37 - 04:45  (10:08)
reboot   system boot  6.6.114.1-micros Thu Jun  4 10:41 - 10:41  (00:00)
reboot   system boot  6.6.114.1-micros Fri May 15 17:21 - 17:24  (00:03)
reboot   system boot  5.15.167.4-micro Sat Apr 19 09:59 - 17:24 (391+07:25)
reboot   system boot  5.15.167.4-micro Fri Apr 18 15:39 - 17:24 (392+01:45)
reboot   system boot  5.15.167.4-micro Sun Apr  6 10:42 - 17:24 (404+06:42)
reboot   system boot  5.15.167.4-micro Sun Mar 16 12:53 - 17:24 (425+04:31)
reboot   system boot  5.15.167.4-micro Sat Mar 15 09:29 - 17:24 (426+07:54)
reboot   system boot  5.15.167.4-micro Thu Mar 13 17:10 - 17:24 (428+00:14)
reboot   system boot  5.15.167.4-micro Tue Mar 11 07:43 - 17:24 (430+09:41)
reboot   system boot  5.15.167.4-micro Sun Mar  9 05:51 - 17:24 (432+11:33)
reboot   system boot  5.15.167.4-micro Sun Mar  9 05:50 - 17:24 (432+11:34)
deleted more lines...

wtmp begins Thu Jan 23 18:07:24 2025
```
 
##### To check the current user name and system version

```bash
username@hostname:~$ uname -a

Linux DESKTOP-3ORSLE9 6.18.33.2-microsoft-standard-WSL2 #1 SMP PREEMPT_DYNAMIC Thu Jun 18 21:54:43 UTC 2026 x86_64 x86_64 x86_64 GNU/Linux
```

##### To check the current kernel version

```bash
username@hostname:~$ uname -r

6.18.33.2-microsoft-standard-WSL2
```


>Here is the breakdown of what that long string of information actually tells you:

```
| **Field** | **Option** | **Description** | **Example Output** |
| --- | --- | --- | --- |
| Kernel name | ``-s`` | Operating system kernel name | ``Linux`` |
| Hostname (nodename) | ``-n`` | System’s network node name (same as ``hostname``) | ``myserver.local`` |
| Kernel release | ``-r`` | Kernel release number | ``6.8.0-51-generic`` |
| Kernel version | ``-v`` | Build details: version, SMP info, build date | ``#52-Ubuntu ``SMP ``PREEMPT_DYNAMIC ``Thu ``Dec ``5 ``13:09:44 ``UTC ``2024`` |
| Machine hardware name | ``-m`` | Hardware architecture | ``x86_64`` |
| Processor type | ``-p`` | Processor type (may be ``unknown`` on some systems) | ``x86_64`` |
| Hardware platform | ``-i`` | Hardware platform (often same as machine) | ``x86_64`` |
| Operating system | ``-o`` | OS name | ``GNU/Linux`` |


```
##### ps command used for manage processes

```bash
username@hostname:~$ ps

    PID TTY          TIME CMD
   1054 pts/2    00:00:00 bash
   1947 pts/2    00:00:00 ps

   ```
```bash
username@hostname:~$ ps -ef

UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 09:32 ?        00:00:01 /sbin/init
root           2       1  0 09:32 hvc0     00:00:00 /init
root           7       2  0 09:32 hvc0     00:00:00 plan9 --control-socket 7 --log-level 4 --server-fd 8 --pipe-fd 10 --log-truncate
root          56       1  0 09:32 ?        00:00:01 /usr/lib/systemd/systemd-journald
root         104       1  0 09:32 ?        00:00:05 /usr/lib/systemd/systemd-udevd
root         117       1  0 09:32 ?        00:00:00 snapfuse /var/lib/snapd/snaps/core24_1587.snap /snap/core24/1587 -o ro,nodev,allow_other,suid
root         118       1  0 09:32 ?        00:00:00 snapfuse /var/lib/snapd/snaps/core24_1643.snap /snap/core24/1643 -o ro,nodev,allow_other,suid
root         131       1  0 09:32 ?        00:00:03 snapfuse /var/lib/snapd/snaps/snapd_26865.snap /snap/snapd/26865 -o ro,nodev,allow_other,suid
root         134       1  0 09:32 ?        00:00:00 snapfuse /var/lib/snapd/snaps/tldr_666.snap /snap/tldr/666 -o ro,nodev,allow_other,suid
root         138       1  0 09:32 ?        00:00:00 snapfuse /var/lib/snapd/snaps/tldr_791.snap /snap/tldr/791 -o ro,nodev,allow_other,suid
systemd+     220       1  0 09:32 ?        00:00:00 /usr/lib/systemd/systemd-resolved
systemd+     221       1  0 09:32 ?        00:00:00 /usr/lib/systemd/systemd-timesyncd
root         230       1  0 09:32 ?        00:00:00 /usr/sbin/cron -f -P
message+     231       1  0 09:32 ?        00:00:00 @dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation --syslog-only
root         244       1  0 09:32 ?        00:00:00 /usr/lib/systemd/systemd-logind
root         249       1  0 09:32 ?        00:00:00 /usr/libexec/wsl-pro-service -vv
syslog       269       1  0 09:32 ?        00:00:00 /usr/sbin/rsyslogd -n -iNONE
```
##### To check to process named systemd
```bash
username@hostname:~$ ps -ef |grep systemd

root          56       1  0 09:32 ?        00:00:01 /usr/lib/systemd/systemd-journald
root         104       1  0 09:32 ?        00:00:05 /usr/lib/systemd/systemd-udevd
systemd+     220       1  0 09:32 ?        00:00:00 /usr/lib/systemd/systemd-resolved
systemd+     221       1  0 09:32 ?        00:00:00 /usr/lib/systemd/systemd-timesyncd
message+     231       1  0 09:32 ?        00:00:00 @dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation --syslog-only
root         244       1  0 09:32 ?        00:00:00 /usr/lib/systemd/systemd-logind
arvind       521       1  0 09:32 ?        00:00:00 /usr/lib/systemd/systemd --user
arvind      1992    1054  0 12:38 pts/2    00:00:00 grep --color=auto systemd

```
##### KIlling a process using `kill` command

```bash
username@hostname:~$ ps -ef |grep tail

arvind      1997    1386  0 12:42 pts/3    00:00:00 tail -f meminfo
arvind      2002    1054  0 12:43 pts/2    00:00:00 grep --color=auto tail
username@hostname:~$ kill 1997

username@hostname:~$ ps -ef |grep tail

arvind      2004    1054  0 12:44 pts/2    00:00:00 grep --color=auto tail
username@hostname:~$ ps -ef |grep tail

arvind      2005    1386  0 12:45 pts/3    00:00:00 tail -f meminfo
arvind      2007    1054  0 12:45 pts/2    00:00:00 grep --color=auto tail
username@hostname:~$ kill -9 2005

username@hostname:~$ ps -ef |grep tail

arvind      2009    1054  0 12:46 pts/2    00:00:00 grep --color=auto tail
```

>[!NOTE] Use -9 for hard kill and -9 -1 for self kill
 - kill -9 forcefully and immediately terminates a specific process by its ID number without allowing it to save data or clean up. 
 - kill -9 -1 forcefully and immediately terminates every single process that your current user has permission to kill, effectively logging you out or crashing  your current session.


```bash
username@hostname:~$ echo arvind

arvind

username@hostname:~$ echo $arvind

username@hostname:~$ arvind=78778

username@hostname:~$ echo $arvind

78778
```
##### Show the proccess id current user
```bash
username@hostname:~$ echo $$

1054




username@hostname:~$ ps -ef 

UID          PID    PPID  C STIME TTY          TIME CMD

arvind      1054    1053  0 09:54 pts/2    00:00:00 bash -i
root        1378       2  0 10:35 ?        00:00:00 /init
root        1380    1378  0 10:35 ?        00:00:00 /init
arvind      1386    1380  0 10:35 pts/3    00:00:00 -bash
arvind      2014    1054  0 12:54 pts/2    00:00:00 ps -ef
```
##### Show the shell name
```bash
username@hostname:~$ echo $0

bash

```



`$1, $2, $3...: Positional parameters representing the arguments passed to a script. $1 is the first argument, $2 is the second, etc.`

Example:- ./script.sh arg1 arg2 arg3

`$#: The total number of arguments passed to a script or function`

`$*: All arguments passed to the script, grouped together as a single string ("$1 $2 $3").`


` $@: All arguments passed to the script, treated as separate, individually quoted strings ("$1" "$2" "$3").`

`$?: The exit status of the most recently executed command. 0 means success; anything else (usually 1 to 255) indicates an error. `                                                                        .

`$!: The Process ID (PID) of the most recent background job/process you ran (e.g., a command ended with &).`

```bash
username@hostname:~$ echo $-

himBHs
```


`$- The current flags/options enabled in your shell (useful for debugging script behavior).`

### `!!` - Repeat Last Command
```bash
username@hostname:~$ !!
```

---

### `id` - Display User Identity
```bash
username@hostname:~$ id
uid=1000(arvind) gid=1000(arvind) groups=1000(arvind),4(adm),20(dialout),24(cdrom),25(floppy),27(sudo),29(audio),30(dip),44(video),46(plugdev),100(users),107(netdev)
```

The `id` command displays the real and effective user identities (UID) and group identities (GID) of a user.

#### Understanding the Output

| Field | Description |
|-------|-------------|
| `uid=1000(arvind)` | **User ID** - Unique numeric ID (1000) mapped to username `arvind`. Root is always `uid=0`. |
| `gid=1000(arvind)` | **Primary Group ID** - Default group for new files/directories. Linux creates a private group matching the username. |
| `groups=...` | **Supplementary Groups** - All groups the user belongs to; determines permissions. |

**Key supplementary groups:**
- `27(sudo)` - Allows administrative commands via `sudo`
- `4(adm)` - Allows reading system log files
- `20(dialout)` - Access to serial ports/modems
- `24(cdrom)` - Access to CD-ROM drives
- `46(plugdev)` - Access to pluggable devices

#### Useful Variations
```bash
id username              # Check specific user (e.g., id root)
id -u                    # Numeric UID only (useful in scripts)
id -un                   # Username only
id -Gn                   # All group names (clean list)
```

---

### Runlevels (SysV init / systemd targets)
```bash
username@hostname:~$ : << 'eof'
```

These numbers refer to SysV init runlevels (or their systemd target equivalents), which define the system state after booting:

| Runlevel | Target | Description |
|----------|--------|-------------|
| `0` | `poweroff.target` | Completely shuts down and powers off the system |
| `1` | `rescue.target` | Single-user mode (rescue) with root terminal, no networking |
| `2` | `multi-user.target` | Multi-user mode without networking (rarely used) |
| `3` | `multi-user.target` | Full multi-user mode with networking, text-based CLI (servers) |
| `4` | *(undefined)* | Customizable for user-specific/local configurations |
| `5` | `graphical.target` | Full multi-user mode with networking and GUI (desktops) |
| `6` | `reboot.target` | Safely stops services and reboots |

```bash
> eof
```

---

### `write` / `wall` - Broadcast Messages
```bash
username@hostname:~$ write "please logout from the system"
write: effective gid does not match group of /dev/pts/2

username@hostname:~$ wall "please logout from the system"

username@hostname:~$ echo "please logout from the system" | wall
```

- **`write`** - Send message to a specific user's terminal (requires same group on tty)
- **`wall`** - Broadcast message to all logged-in users (Write ALL)

---

### User Management

#### `useradd` - Create New User
```bash
username@hostname:~$ useradd task_user1
useradd: Permission denied.
useradd: cannot lock /etc/passwd; try again later.

username@hostname:~$ sudo useradd task_user1
[sudo] password for arvind:
```

#### `passwd` - Set/Change Password
```bash
username@hostname:~$ passwd task_user1
passwd: You may not view or modify password information for task_user1.

username@hostname:~$ sudo passwd task_user1
```

> **Note:** Use `sudo` for administrative commands.
---

### User Management (continued)

#### `su` - Switch User
```bash
username@hostname:~$ su task_user1
Password:
$ whoami
task_user1
$ exit
username@hostname:~$ whoami
arvind
```

#### `sudo su` - Switch to Root
```bash
username@hostname:~$ sudo su
root
uid=0(root) gid=0(root) groups=0(root)
exit

exit
```

#### `id` - Check User Identity
```bash
username@hostname:~$ id task_user1
uid=1001(task_user1) gid=1001(task_user1) groups=1001(task_user1)
```

#### `userdel` - Delete User
```bash
username@hostname:~$ sudo userdel task_user1
username@hostname:~$ su task_user1
su: user task_user1 does not exist or the user entry does not contain all the required fields
```

#### `cat /etc/passwd` - List All Users
```bash
username@hostname:~$ cat /etc/passwd
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
# ... (truncated for brevity)
arvind:x:1000:1000:,,,:/home/arvind:/bin/bash
```

> **Note:** `cat /etc/passwd` shows all user accounts on the system. Each line has 7 fields separated by `:`.

---

### User Management - Day 2

#### `su` and `sudo su -` with Root Environment
```bash
username@hostname:~$ sudo su
root@DESKTOP-3ORSLE9:/home/arvind# pwd
/home/arvind
root@DESKTOP-3ORSLE9:/home/arvind# exit
exit
username@hostname:~$ sudo su -
Welcome to Ubuntu 24.04.4 LTS ...
root@DESKTOP-3ORSLE9:~# pwd
/root
root@DESKTOP-3ORSLE9:~# exit
logout
```

> **`sudo su`** keeps the current directory. **`sudo su -`** switches to root's home directory (`/root`).

#### Creating User with Home Directory
```bash
username@hostname:~$ sudo useradd robot1
username@hostname:~$ sudo passwd robot1
New password:
Retype new password:
passwd: password updated successfully
username@hostname:~$ sudo useradd -m robot1
useradd: user 'robot1' already exists
username@hostname:~$ sudo userdel robot1
username@hostname:~$ sudo useradd -m robot1
username@hostname:~$ sudo passwd robot1
```

> **`useradd -m robot1`** creates the user with a home directory (`/home/robot1`).

#### Changing User Shell with `usermod`
```bash
username@hostname:~$ sudo usermod -s /bin/bash robot1
username@hostname:~$ cat /etc/passwd | grep robot1
robot1:x:1001:1001::/home/robot1:/bin/bash
```

#### Lock/Unlock User
```bash
username@hostname:~$ sudo usermod -L robot1    # Lock user
username@hostname:~$ su robot1
Password:
su: Authentication failure
username@hostname:~$ sudo usermod -U robot1    # Unlock user
username@hostname:~$ su robot1
Password:
robot1@DESKTOP-3ORSLE9:/home/arvind$ exit
exit
```

---

### File Operations

#### `cp` - Copy Files
```bash
username@hostname:~$ cp -v abc.txt project1
'abc.txt' -> 'project1/abc.txt'
username@hostname:~$ cp abc.txt project1
```

#### `mv` - Move/Rename Files
```bash
username@hostname:~$ mv abc.txt abc.log
username@hostname:~$ mv abcd.txt abcd.log
username@hostname:~$ mv abc.txt abc.log && abcd.txt abcd.log
mv: cannot stat 'abc.txt': No such file or directory
username@hostname:~$ mv doucment/abd doucment/radio
```

#### `rm` - Remove Files/Directories
```bash
username@hostname:~$ rm project1/abc.txt
username@hostname:~$ rm project1
rm: cannot remove 'project1': Is a directory
username@hostname:~$ rm -fir project1
rm: descend into directory 'project1'? y
rm: remove regular file 'project1/abc.txt'? y
rm: remove directory 'project1/fortend'? y
rm: remove directory 'project1'? y
```

#### `chmod` - Change File Permissions
```bash
username@hostname:~$ chmod 755 abcd.txt
username@hostname:~$ chmod 777 abcd.txt
username@hostname:~$ chmod o-x abcd.txt          # Remove execute for others
username@hostname:~$ chmod u+x abcd.txt           # Add execute for owner
username@hostname:~$ chmod -x -u abcd.txt         # Remove execute from owner
```

> **Permission structure:** `---` (owner) `---` (group) `---` (others)  
> **Values:** read=4, write=2, execute=1

#### `getfacl` - View File ACL
```bash
username@hostname:~$ getfacl abcd.txt
# file: abcd.txt
# owner: arvind
# group: arvind
user::rwx
group::rwx
other::rw-
```

#### `chown` / `chgrp` - Change Owner/Group
```bash
username@hostname:~$ sudo chown robot1 abd
username@hostname:~$ sudo chgrp robot1 abd
username@hostname:~$ sudo chown arvind:arvind abd    # Change both owner and group in one command
```

---

### Text Processing Commands

#### `grep` - Search Text
```bash
username@hostname:~$ grep -il server *.log          # Case-insensitive, show filenames only
username@hostname:~$ grep -il Server *.log
username@hostname:~$ grep -in server *.log          # Show line numbers
abcd.log:61:• Are you configuring a web server or a private script?
username@hostname:~$ grep -iv server *.log          # Invert match (show lines NOT containing)
username@hostname:~$ grep -ivl server *.log         # Files NOT containing match
username@hostname:~$ grep -in ^Advance *.log        # Lines starting with "Advance"
abcd.log:44:Advanced system states can be appended...
```

#### `sort` - Sort Lines
```bash
username@hostname:~$ sort -n numbers                # Numeric sort
1
2
3
3
4
5
7
username@hostname:~$ sort -nr numbers               # Reverse numeric sort
7
5
4
3
3
2
1
```

#### `uniq` - Remove Duplicates
```bash
username@hostname:~$ sort -n numbers | uniq
1
2
3
4
5
7
```

#### `wc` - Word Count
```bash
username@hostname:~$ wc -l abcd.log                 # Line count
94 abcd.log
username@hostname:~$ wc -w abcd.log                 # Word count
593 abcd.log
username@hostname:~$ wc -c abcd.log                 # Byte count
4941 abcd.log
```

#### `cut` - Cut Selected Characters/Fields
```bash
username@hostname:~$ cut -c 1-4 abc.log             # Characters 1-4
bada
username@hostname:~$ cut -d ':' -f 1 /etc/passwd    # Field 1 (usernames), delimiter ':'
username@hostname:~$ cut -d ':' -f 7 /etc/passwd    # Field 7 (shells)
```

> **`-d`** for delimiter, **`-f`** for field/column number

#### `head` / `tail` - Head/Tail of Files
```bash
username@hostname:~$ head z
username@hostname:~$ head -4 z
username@hostname:~$ tail z
username@hostname:~$ tail -n 2 z
username@hostname:~$ tail -f linux_basic_commands.txt    # Follow mode (live update)
```

#### `paste` - Merge Lines of Files
```bash
username@hostname:~$ cat new
rohan
mohan
riya
siya
username@hostname:~$ cat new2
geeta
sita
pintu
ritu
username@hostname:~$ paste new new2
rohan   geeta
mohan   sita
riya    pintu
siya    ritu
```

#### `diff` - Compare Files
```bash
username@hostname:~$ diff acd abd
1c1
< rohan geeta
---
> geeta reta
```

---

### Compression / Archiving

#### `tar` - Archive Files
```bash
username@hostname:~$ tar -cvf abcd.tar abcd.log         # Create tar archive
abcd.log
username@hostname:~$ tar -cvfz abcd.tar.gz abcd.log     # Create tar.gz archive
```

#### `gzip` - Compress Files
```bash
username@hostname:~$ gzip abcd.log                      # Compress (replaces file with .gz)
username@hostname:~$ ls -lrt abcd.log.gz
-rwxrwxrw- 1 arvind arvind 2251 Jul  8 07:06 abcd.log.gz
```

> Compression formats: `.zip` (cross-platform), `.tar.gz` (standard Linux), `.gz` (single-file fast), `.tar.xz` (maximum compression)

---

### Package Management

#### `apt list` - Search Packages
```bash
username@hostname:~$ sudo apt list ssh
Listing... Done
ssh/noble-updates,noble-security 1:9.6p1-3ubuntu13.8 all
username@hostname:~$ sudo apt list cal
Listing... Done
```

#### `apt install` - Install Packages
```bash
username@hostname:~$ sudo apt install ncal
# Package installed successfully
username@hostname:~$ cal
     July 2026
Su Mo Tu We Th Fr Sa
          1  2  3  4
 5  6  7  8  9 10 11
...
```

> **`sudo apt update`** - Update package manager cache  
> **`sudo apt upgrade`** - Upgrade all packages to latest version  
> **`sudo apt remove <package>`** - Remove a package  
> **`sudo apt autoremove`** - Remove dependency files for deleted packages

---

### Service Management

#### `systemctl` - Manage System Services
```bash
username@hostname:~$ systemctl status cron
● cron.service - Regular background program processing daemon
     Loaded: loaded (/usr/lib/systemd/system/cron.service; enabled; preset: enabled)
     Active: active (running) since Tue 2026-07-07 17:29:55 UTC; 43min ago
       Docs: man:cron(8)
   Main PID: 224 (cron)

username@hostname:~$ systemctl reload cron
Failed to reload cron.service: Interactive authentication required.

username@hostname:~$ sudo systemctl reload cron
Failed to reload cron.service: Job type reload is not applicable for unit cron.service.

username@hostname:~$ sudo systemctl restart cron
```

##### Managing Services (Units)
| Command | Description |
|---------|-------------|
| `systemctl start <service>` | Start a service |
| `systemctl stop <service>` | Stop a service |
| `systemctl restart <service>` | Restart a service |
| `systemctl reload <service>` | Reload configuration without stopping |
| `systemctl status <service>` | Check service status |
| `systemctl enable <service>` | Enable auto-start at boot |
| `systemctl disable <service>` | Disable auto-start at boot |
| `systemctl mask <service>` | Prevent service from starting |
| `systemctl unmask <service>` | Remove mask |
| `systemctl list-units --type=service` | List all active services |
| `systemctl list-unit-files --type=service` | List all installed services |
| `systemctl daemon-reload` | Reload systemd configuration |
| `systemctl reboot` | Reboot system |
| `systemctl poweroff` | Power off system |

#### `service` - Legacy Service Management
```bash
username@hostname:~$ service --status-all
 [ - ]  apparmor
 [ + ]  cron
 [ + ]  dbus
 [ + ]  kmod
 [ - ]  rsync
 [ + ]  unattended-upgrades
```

---

### Shell Variables and Environment

#### Variables
```bash
username@hostname:~$ a=arvind
username@hostname:~$ echo $a
arvind
username@hostname:~$ a='arvind kumar'
username@hostname:~$ echo $a
arvind kumar
username@hostname:~$ echo $HOME
/home/arvind
username@hostname:~$ echo $SHELL
/bin/bash
```

> **Note:** Variable values are accessed using `$` prefix. No spaces around `=` when assigning.

#### Arithmetic
```bash
username@hostname:~$ echo $((5+6))
11
username@hostname:~$ expr 4 + 6
10
username@hostname:~$ expr 4 \* 6                     # Escaped asterisk for multiplication
24
username@hostname:~$ abc=`expr 4 \* 6`                # Backtick command substitution
username@hostname:~$ echo $abc
24
```

#### PATH and `export`
```bash
username@hostname:~$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:...

username@hostname:~$ export PATH=/home/arvind          # Set PATH (temporary)
username@hostname:~$ prtn
sorty
username@hostname:~$ ls
Command 'ls' is available in the following places
 * /bin/ls
 * /usr/bin/ls
The command could not be located because '/usr/bin:/bin' is not included in the PATH.

username@hostname:~$ export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin  # Restore PATH
```

> To permanently set PATH, edit `~/.bashrc` or `~/.bash_profile` and add: `PATH=$PATH:$HOME/bin:.`

---

### Aliases
```bash
username@hostname:~$ alias pri='cd /home/arvind/project1/fortend'
username@hostname:~$ alias
alias alert='notify-send ...'
alias egrep='egrep --color=auto'
alias grep='grep --color=auto'
alias l='ls -l'
alias la='ls -A'
alias ll='ls -alF'
alias ls='ls --color=auto'
alias pri='cd /home/arvind/project1/fortend'
alias whome='cd /mnt/c/users/Alpha_320'
```

---

### `ifconfig` - Network Interface Info
```bash
username@hostname:~$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 172.18.143.30  netmask 255.255.240.0  broadcast 172.18.143.255
        ether 00:15:5d:6b:73:7c  txqueuelen 1000  (Ethernet)

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
```

---

### `cal` - Calendar Display
```bash
username@hostname:~$ cal
     July 2026
Su Mo Tu We Th Fr Sa
          1  2  3  4
 5  6  7  8  9 10 11
...

username@hostname:~$ cal june 2026
username@hostname:~$ cal 2026
username@hostname:~$ cal 09 1952
```

---

### `telnet` - Remote Login
```bash
username@hostname:~$ telnet
telnet> ?
Commands may be abbreviated.  Commands are:
close           close current connection
logout          forcibly logout remote user and close the connection
display         display operating parameters
open            connect to a site
quit            exit telnet
status          print status information
...
telnet> quit
```

---

### `which` / `whereis` - Locate Commands
```bash
username@hostname:~$ which ls
/usr/bin/ls
username@hostname:~$ which cd                              # Shell built-in (no path)
username@hostname:~$ whereis grep
grep: /usr/bin/grep /usr/share/man/man1/grep.1.gz /usr/share/info/grep.info.gz
```

---

### Input/Output Redirection

#### `>` / `>>` / `2>` / `&>` - Redirect Output
```bash
username@hostname:~$ echo "hoououoo" > testfile2           # Overwrite
username@hostname:~$ echo "hluluooolili" >> testfile2      # Append
username@hostname:~$ cat gdhgd 2> testfile2                # Redirect stderr
username@hostname:~$ cat gdhgd > testfile2                 # Error goes to terminal
username@hostname:~$ cat testfile2 &> testfile2            # Redirect both stdout and stderr
```

#### `<< 'EOF'` - Here Document
```bash
username@hostname:~$ cat << 'EOF' > testfile2
> this is the test file creation and putting content inside using single command
> EOF
```

---

### `read` - Read Input
```bash
username@hostname:~$ read
Arvind kumar
username@hostname:~$ echo $REPLY
Arvind kumar
```

> If no variable is given, the value gets assigned to the built-in variable `REPLY`.

---

### Shell Script Debugging
```bash
bash -x ./hello.sh
```

> Or use `set -x` at the start of the line to debug, then `set +x` at the end.

---

### Other Useful Commands

#### `watch` - Run Command Repeatedly
```bash
username@hostname:~$ watch 'ls -lrt'
```

#### `at` - Schedule One-Time Jobs
```bash
username@hostname:~$ at now + 1 minute
warning: commands will be executed using /bin/sh
at> echo "hello"
at> <EOT>
job 1 at Thu Jul  9 18:04:00 2026
```

#### `crontab` - Schedule Recurring Jobs
```bash
username@hostname:~$ crontab -l                    # List cron jobs
username@hostname:~$ crontab -e                    # Edit cron file
```

#### `printenv` / `env` - Print Environment Variables
```bash
username@hostname:~$ printenv
SHELL=/bin/bash
HOME=/home/arvind
PATH=...
USER=arvind
...
```

> `env` and `printenv` work the same.

#### `lscpu` - CPU Information
```bash
username@hostname:~$ lscpu
Architecture:        x86_64
CPU(s):              12
Model name:          AMD Ryzen 5 7535HS with Radeon Graphics
```

#### `nano` / `vi` - Text Editors
```bash
username@hostname:~$ nano abcd.txt
username@home:~$ vi .bashrc
```

> In nano: `Ctrl+S` to save, `Ctrl+X` to exit.  
> vi and nano are editors in Linux — refer to separate documentation for detailed usage.

---

### `script` - Record Terminal Activity
```bash
script <filename>        # Start recording
# ... run commands ...
# Press Ctrl+D to stop recording
```

---

### Networking Commands
- `netstat`, `ping`, `ftp`, `sftp`, `traceroute`, `tracert`, `ifconfig`, `nslookup`, `hostname`, `dig`, `tcpdump`, `curl`

---

### User Management Commands Summary
| Command | Description |
|---------|-------------|
| `sudo usermod -u <1234> <username>` | Change user ID |
| `sudo usermod -l <new> <old>` | Change username |
| `chfn` | Change user's personal information |
| `chsh` | Change user's shell |
| `groupadd` / `groupdel` | Add/delete user group |
| `sudo usermod -L <user>` | Lock user account |
| `sudo usermod -U <user>` | Unlock user account |

---

### Execute Multiple Commands
```bash
cmd1; cmd2; cmd3; ...
```

---

### `ls` Filtering Examples
```bash
ls -lrt | grep ^-              # Show only files
ls -lrt | grep ^d              # Show only directories
ls -lrt | grep sh$             # Show only .sh files
```

---

## DevOps & Administration Essentials

---

### Firewall: `ufw` (Uncomplicated Firewall)
```bash
sudo ufw status                        # Check firewall status
sudo ufw status verbose                # Detailed status with policy
sudo ufw enable                        # Enable firewall (CAUTION: may lock SSH)
sudo ufw disable                       # Disable firewall

# Allow/Deny by Port
sudo ufw allow 22                      # Allow SSH port
sudo ufw allow 80/tcp                  # Allow HTTP on TCP
sudo ufw allow 443                     # Allow HTTPS
sudo ufw deny 23                       # Block Telnet port

# Allow/Deny by IP
sudo ufw allow from 192.168.1.100              # Allow all traffic from specific IP
sudo ufw deny from 10.0.0.50                   # Block specific IP
sudo ufw allow from 192.168.1.0/24 to any port 22  # Allow subnet to SSH

# Allow by Application Profile
sudo ufw app list                      # List available app profiles
sudo ufw allow 'OpenSSH'               # Allow OpenSSH profile

# Rules Management
sudo ufw delete allow 80               # Delete a rule
sudo ufw reset                         # Reset all rules to default
sudo ufw default deny incoming         # Default policy: deny incoming
sudo ufw default allow outgoing        # Default policy: allow outgoing
```

---

### Firewall: `iptables` (Low-Level)
```bash
# List Rules
sudo iptables -L -n -v                 # List rules with counters
sudo iptables -t nat -L -n             # List NAT table rules

# Chain Policy
sudo iptables -P INPUT DROP            # Default: drop all incoming
sudo iptables -P FORWARD DROP          # Default: drop forwarded
sudo iptables -P OUTPUT ACCEPT         # Default: allow outgoing

# Allow Rules
sudo iptables -A INPUT -i lo -j ACCEPT                    # Allow loopback
sudo iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT  # Allow established
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT        # Allow SSH
sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT        # Allow HTTP
sudo iptables -A INPUT -s 192.168.1.0/24 -j ACCEPT        # Allow subnet

# Block Rules
sudo iptables -A INPUT -s 10.0.0.50 -j DROP              # Block IP
sudo iptables -A INPUT -p tcp --dport 23 -j DROP         # Block Telnet

# Save & Restore
sudo iptables-save > /etc/iptables/rules.v4              # Save rules
sudo iptables-restore < /etc/iptables/rules.v4           # Restore rules
```

---

### SSH Key Management
```bash
# Generate Key Pair
ssh-keygen -t ed25519 -C "your@email.com"               # ED25519 (recommended)
ssh-keygen -t rsa -b 4096 -C "your@email.com"           # RSA 4096-bit

# Copy Public Key to Remote Server
ssh-copy-id user@remote-server                          # Copy key (password required once)
ssh-copy-id -i ~/.ssh/id_ed25519.pub user@remote-server # Specify key file

# SSH Config File (~/.ssh/config)
cat << 'EOF' >> ~/.ssh/config
Host myserver
    HostName 192.168.1.100
    User ubuntu
    Port 22
    IdentityFile ~/.ssh/id_ed25519
EOF
ssh myserver                                             # Connect using alias

# SSH Tunneling (Port Forwarding)
ssh -L 8080:localhost:80 user@remote     # Local port 8080 → remote 80
ssh -R 8080:localhost:80 user@remote     # Remote port 8080 → local 80
ssh -D 1080 user@remote                  # SOCKS5 proxy on local port 1080

# Key Permissions (must be correct)
chmod 600 ~/.ssh/id_ed25519             # Private key
chmod 644 ~/.ssh/id_ed25519.pub         # Public key
chmod 700 ~/.ssh                         # SSH directory
```

---

### Sudoers Configuration
```bash
sudo visudo                              # Edit sudoers safely (always use visudo!)

# Common sudoers entries:
# /etc/sudoers or /etc/sudoers.d/custom
username ALL=(ALL) ALL                   # User gets full sudo access
%admin ALL=(ALL) ALL                     # Group gets sudo access
username ALL=(ALL) NOPASSWD: ALL         # No password for sudo
username ALL=(ALL) NOPASSWD: /bin/systemctl, /bin/apt  # No passwd for specific cmds
%deploy ALL=(ALL) NOPASSWD: /usr/bin/docker  # Group can run docker without password
```

---

### Process Monitoring

#### `top` / `htop` - Real-Time Process Viewer
```bash
top                                      # Interactive process viewer
  # Inside top:  h=help, q=quit, k=kill process, r=renice, u=filter by user
  #              M=sort by memory, P=sort by CPU, 1=show per-core

htop                                     # Enhanced top (install via: sudo apt install htop)
```

#### `ps` Advanced Usage
```bash
ps aux                                   # All processes (BSD format)
ps aux --sort=-%mem                      # Sort by memory usage
ps aux --sort=-%cpu                      # Sort by CPU usage
ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%cpu | head -10  # Top 10 CPU processes
ps -u username -o pid,cmd               # Processes for specific user
```

#### `kill` / `killall` / `pkill`
```bash
kill -15 PID                             # Graceful terminate (SIGTERM)
kill -9 PID                              # Force kill (SIGKILL)
killall nginx                            # Kill all processes named nginx
pkill -f "python script.py"              # Kill by full command name
pkill -u username                        # Kill all processes by user
```

---

### Disk & Filesystem Management

#### `lsblk` / `blkid` - Block Device Info
```bash
lsblk                                    # List block devices (tree view)
lsblk -f                                 # Show filesystem type and UUID
blkid                                    # Show UUID and filesystem of devices
```

#### `df` / `du` - Disk Usage
```bash
df -h                                    # Human-readable disk usage (all mounts)
df -hT                                   # Show filesystem type
du -sh /var/log                          # Size of directory
du -h --max-depth=1 /home               # Size of immediate subdirectories
du -ah /var/log | sort -rh | head -10   # Top 10 largest files in /var/log
```

#### `mount` / `umount` - Mount Filesystems
```bash
mount                                    # List all mounted filesystems
sudo mount /dev/sdb1 /mnt/data          # Mount device to directory
sudo mount -t nfs 192.168.1.10:/share /mnt/nfs  # Mount NFS share
sudo umount /mnt/data                   # Unmount
sudo umount -l /mnt/data                # Lazy unmount (when device is busy)
```

#### `fdisk` - Partition Management
```bash
sudo fdisk -l                            # List all partitions and disks
sudo fdisk /dev/sdb                      # Interactive partition tool
  # Inside: m=help, n=new partition, d=delete, w=write, q=quit

sudo mkfs.ext4 /dev/sdb1                # Format partition as ext4
sudo mkfs.xfs /dev/sdb2                 # Format partition as xfs
```

#### Swap Management
```bash
swapon --show                           # Show active swap
sudo swapon /swapfile                   # Enable swap file
sudo swapoff /swapfile                  # Disable swap file
sudo fallocate -l 2G /swapfile          # Create 2GB swap file
sudo mkswap /swapfile                   # Format as swap
```

---

### System Logging

#### `journalctl` - systemd Journal
```bash
journalctl                               # View all logs
journalctl -u cron.service               # Logs for specific service
journalctl -u nginx.service --since "1 hour ago"  # Last hour
journalctl -u ssh.service -f             # Follow (tail -f) mode
journalctl -k                            # Kernel logs
journalctl --disk-usage                  # Log size on disk
journalctl -u docker.service -o json-pretty  # JSON format output
sudo journalctl --vacuum-size=500M      # Trim logs to 500MB
```

#### Log Files Location
| Log | Path | Purpose |
|-----|------|---------|
| System | `/var/log/syslog` | General system logs |
| Auth | `/var/log/auth.log` | Login attempts, sudo usage |
| Kernel | `/var/log/kern.log` | Kernel messages |
| Package | `/var/log/dpkg.log` | Package install/remove history |
| Nginx | `/var/log/nginx/access.log` | Web server access |
| Nginx | `/var/log/nginx/error.log` | Web server errors |

---

### Performance Monitoring

#### `vmstat` - Virtual Memory Stats
```bash
vmstat 2                                 # Report every 2 seconds
vmstat -s                                # Event counters summary
```
Output: `procs - memory - swap - io - system - cpu`

#### `iostat` - I/O Stats
```bash
iostat -x 2                              # Extended I/O stats every 2s
iostat -p sda 2                          # Stats for specific disk
```

#### `sar` - System Activity Reporter
```bash
sar -u 2 5                               # CPU usage, 5 samples at 2s interval
sar -r 2 5                               # Memory usage
sar -b 2 5                               # I/O activity
sar -n DEV 2 5                           # Network interface stats
sar -S 2 5                               # Swap usage
sar -q 2 5                               # Load average and queue
```

#### `mpstat` - Multi-Processor Stats
```bash
mpstat -P ALL 2                          # Per-CPU usage every 2s
```

#### `netstat` / `ss` - Network Connections
```bash
ss -tulpn                                # All listening TCP/UDP sockets (modern)
ss -tup                                  # Active connections
ss -s                                    # Connection summary
netstat -tulpn                           # All listening ports (legacy)
netstat -i                               # Interface statistics
```

---

### Network Diagnostics

#### `ping` / `traceroute` / `mtr`
```bash
ping -c 4 google.com                     # Send 4 ICMP packets
ping -i 0.5 google.com                   # Interval 0.5s (root only)
traceroute google.com                    # Trace network path (ICMP)
traceroute -T google.com                 # TCP traceroute
mtr google.com                           # Continuous trace + ping (install: sudo apt install mtr)
```

#### `curl` - HTTP API Testing
```bash
curl -I https://api.example.com          # Show response headers only
curl -v https://api.example.com          # Verbose (full request/response)
curl -X POST -H "Content-Type: application/json" -d '{"key":"value"}' https://api.example.com
curl -o file.html https://example.com    # Download to file
curl -u user:pass https://api.example.com/auth  # Basic auth
curl -k https://self-signed.example.com  # Skip SSL verification
curl --connect-timeout 5 https://example.com  # Timeout after 5s
```

#### `wget` - File Download
```bash
wget https://example.com/file.tar.gz              # Download file
wget -O custom-name.tar.gz https://example.com/file  # Download with custom name
wget -c https://example.com/large-file.iso        # Resume interrupted download
wget -r -np -nH --cut-dirs=1 https://example.com/files/  # Recursive download
```

#### `dig` / `nslookup` - DNS Queries
```bash
dig google.com                           # Standard DNS lookup
dig google.com A                         # IPv4 records
dig google.com AAAA                      # IPv6 records
dig google.com MX                        # Mail exchange records
dig -x 8.8.8.8                           # Reverse DNS lookup
dig @1.1.1.1 google.com                 # Query specific DNS server

nslookup google.com                      # Simple DNS lookup
nslookup google.com 8.8.8.8            # Query specific DNS server
host google.com                          # Quick DNS lookup
```

---

### Docker Basics (DevOps Essential)
```bash
# Installation
sudo apt install docker.io               # Install Docker
sudo systemctl enable --now docker       # Enable and start Docker
sudo usermod -aG docker $USER            # Add user to docker group (re-login needed)

# Container Management
docker ps                                # Running containers
docker ps -a                             # All containers
docker images                            # List images
docker pull nginx:alpine                 # Pull image
docker run -d --name web -p 80:80 nginx:alpine  # Run container
docker exec -it web bash                 # Shell into container
docker logs -f web                       # Follow container logs
docker stop web && docker rm web         # Stop and remove container
docker rmi nginx:alpine                  # Remove image

# Docker Compose
docker-compose up -d                     # Start services in background
docker-compose down                      # Stop and remove services
docker-compose logs -f                   # Follow logs
docker-compose ps                        # List services

# Cleanup
docker system prune -a                   # Remove all unused containers, images, networks
docker system df                         # Show disk usage
```

---

### Container Runtime: `podman` (Rootless Alternative)
```bash
podman pull nginx:alpine                 # Pull image (no daemon required)
podman run -d --name web -p 80:80 nginx:alpine  # Run container
podman ps                                # List containers
podman generate systemd --name web > /etc/systemd/system/web-container.service  # Auto-start
```

---

### File Transfer & Sync

#### `rsync` - Remote Sync (Automation)
```bash
rsync -avz source/ user@remote:/dest/             # Sync local → remote
rsync -avz user@remote:/source/ dest/             # Sync remote → local
rsync -avz --delete source/ user@remote:/dest/    # Mirror (delete extraneous files)
rsync -avz -e "ssh -p 2222" source/ user@remote:/dest/  # Custom SSH port
rsync -avz --exclude '*.log' source/ user@remote:/dest/ # Exclude patterns
rsync --dry-run -avz source/ user@remote:/dest/   # Dry-run (test before actual)
```

#### `scp` - Secure Copy
```bash
scp file.txt user@remote:/home/user/              # Copy local → remote
scp user@remote:/home/user/file.txt .             # Copy remote → local
scp -r project/ user@remote:/home/user/           # Copy directory recursively
scp -P 2222 file.txt user@remote:/home/user/      # Custom SSH port
```

---

### Automation Scripting

#### `sed` - Stream Editor (Find & Replace)
```bash
sed -i 's/old-text/new-text/g' file.txt           # Replace all occurrences in-place
sed -n '5,10p' file.txt                           # Print lines 5-10
sed -i '/pattern/d' file.txt                      # Delete lines matching pattern
sed -i 's/^/#/' file.conf                         # Comment out all lines (add #)
sed -i '/^#/d' file.conf                          # Remove all comment lines
```

#### `awk` - Text Processing
```bash
awk '{print $1}' file.txt                         # Print first column
awk -F: '{print $1, $7}' /etc/passwd             # Delimiter : print fields 1 and 7
awk '$3 > 50 {print $1, $3}' file.txt            # Conditional print
awk '{sum+=$3} END {print sum}' file.txt          # Sum of column 3
awk 'NR>1 {print $0}' file.txt                   # Skip header line
```

#### `xargs` - Build & Execute Commands
```bash
find . -name "*.log" | xargs rm -f               # Find and delete log files
cat urls.txt | xargs -n1 curl -O                 # Download each URL
cat ips.txt | xargs -P10 -I{} ping -c1 {}        # Ping 10 IPs in parallel
```

#### `find` - Advanced File Search
```bash
find /var/log -name "*.log" -mtime +7             # Files older than 7 days
find / -type f -size +100M                        # Files larger than 100MB
find /home -user username -type d                 # Directories owned by user
find . -perm /u=r -type f                         # Readable by owner
find /tmp -type f -atime +10 -delete              # Delete files not accessed in 10 days
find . -name "*.py" -exec chmod 755 {} \;         # Execute command on found files
```

---

### System Limits & Resource Control

#### `ulimit` - User Limits
```bash
ulimit -a                                        # Show all current limits
ulimit -n 65535                                  # Increase max open files (temporary)
limit: soft nofile 65535                         # In /etc/security/limits.conf (permanent)
         hard nofile 65535
```

#### `cgroups` - Control Groups (Systemd)
```bash
systemd-cgtop                                   # Show top cgroups by resource
systemd-cgls                                    # Show cgroup tree
systemctl set-property user-1000.slice CPUQuota=50%  # Limit user to 50% CPU
```

---

### Systemd Timers (Modern Cron Replacement)
```bash
# Create a timer: /etc/systemd/system/backup.timer
[Unit]
Description=Daily backup timer

[Timer]
OnCalendar=daily
Persistent=true

[Install]
WantedBy=timers.target

# Enable timer
sudo systemctl daemon-reload
sudo systemctl enable --now backup.timer
sudo systemctl list-timers                    # List all timers
sudo systemctl status backup.timer            # Check timer status
```

---

### Package Managers (Multi-Distro)
```bash
# Debian/Ubuntu (apt/dpkg)
dpkg -l                                        # List all installed packages
dpkg -i package.deb                            # Install .deb file
apt-mark hold package                          # Prevent package from updating
apt-mark unhold package                        # Allow package update

# RHEL/CentOS/Fedora (yum/dnf)
sudo yum install httpd                        # Install package
sudo yum remove httpd                         # Remove package
sudo dnf install nginx                        # Modern Fedora/RHEL
sudo rpm -ivh package.rpm                     # Install RPM file
rpm -qa                                        # List all RPM packages
```

---

### SELinux / AppArmor
```bash
# SELinux (RHEL/CentOS/Fedora)
getenforce                                     # Check SELinux mode
sudo setenforce 0                              # Disable temporarily (permissive)
sudo setenforce 1                              # Enable (enforcing)
semanage port -l                               # List SELinux port contexts
semanage port -a -t http_port_t -p tcp 8080    # Allow Apache on port 8080

# AppArmor (Ubuntu/Debian)
sudo aa-status                                 # Check AppArmor status
sudo apparmor_status                           # List profiles
sudo aa-complain /usr/bin/myservice            # Set to complain (log only) mode
sudo aa-enforce /usr/bin/myservice             # Set to enforce mode
```

---

### Security Hardening

#### Fail2Ban - Brute Force Protection
```bash
sudo apt install fail2ban
sudo cp /etc/fail2ban/jail.conf /etc/fail2ban/jail.local

# /etc/fail2ban/jail.local
[sshd]
enabled = true
port = 22
maxretry = 3
bantime = 3600
findtime = 600

sudo systemctl enable --now fail2ban
sudo fail2ban-client status                   # Check status
sudo fail2ban-client status sshd              # SSH jail status
sudo fail2ban-client set sshd bantime 86400   # Change bantime
```

#### File Integrity
```bash
# Tripwire/AIDE (install via apt)
sudo aideinit                                  # Initialize AIDE database
sudo aide --check                              # Check file integrity
```

---

### System Information Commands

```bash
lsb_release -a                                 # OS/distribution info
hostnamectl                                    # System hostname details
timedatectl                                    # Time/date/timezone status
timedatectl list-timezones                     # List all timezones
localectl                                      # Locale/keyboard settings
dmidecode -t system                            # System hardware info (serial, manufacturer)
lspci                                          # PCI devices
lsusb                                          # USB devices
lsmod                                          # Loaded kernel modules
uname -r                                       # Kernel version
cat /etc/os-release                            # OS release details
```

---

### Special File Permissions (SUID/SGID/Sticky Bit)

| Permission | Numeric | Symbolic | Effect |
|------------|---------|----------|--------|
| **SUID** | `4XXX` | `u+s` | Runs with owner's privileges (e.g., `/usr/bin/passwd`) |
| **SGID** | `2XXX` | `g+s` | Inherits group ownership (e.g., shared directories) |
| **Sticky Bit** | `1XXX` | `o+t` | Only owner can delete files (e.g., `/tmp`) |

```bash
# SUID - Set Owner User ID
chmod u+s /path/to/file                        # Set SUID
chmod 4755 /path/to/file                       # SUID + rwxr-xr-x
find / -perm -4000 -ls                         # Find all SUID binaries

# SGID - Set Group ID
chmod g+s /shared/directory                    # New files inherit group
chmod 2755 /shared/directory                   # SGID + rwxr-xr-x

# Sticky Bit
chmod o+t /shared/directory                    # Only owner can delete
chmod 1777 /tmp                                # Sticky + full access (/tmp standard)
```

---

### Network Configuration (Modern `ip` Command)
```bash
ip addr                                        # Show all IP addresses (replaces ifconfig)
ip addr show eth0                              # IP for specific interface
ip link set eth0 up/down                       # Enable/disable interface
ip route                                       # Show routing table (replaces route -n)
ip route add default via 192.168.1.1           # Set default gateway
ip neigh                                       # ARP table (replaces arp -a)
```

---

### LVM (Logical Volume Manager)
```bash
# Physical Volume
sudo pvcreate /dev/sdb1                        # Create PV
sudo pvs                                       # List PVs

# Volume Group
sudo vgcreate vg_data /dev/sdb1                # Create VG
sudo vgs                                       # List VGs

# Logical Volume
sudo lvcreate -L 50G -n lv_data vg_data        # Create 50GB LV
sudo lvs                                       # List LVs

# Filesystem & Mount
sudo mkfs.ext4 /dev/vg_data/lv_data            # Format LV
sudo mount /dev/vg_data/lv_data /mnt/data      # Mount LV

# Extend LV
sudo lvextend -L +10G /dev/vg_data/lv_data     # Extend by 10GB
sudo lvextend -r -L +10G /dev/vg_data/lv_data  # Extend + resize filesystem
sudo resize2fs /dev/vg_data/lv_data            # Resize ext4 filesystem
```

---

### Ansible Basics (Automation)
```bash
# Install
sudo apt install ansible

# Inventory file (hosts.ini)
[webservers]
web1 ansible_host=192.168.1.10 ansible_user=ubuntu
web2 ansible_host=192.168.1.11 ansible_user=ubuntu

[databases]
db1 ansible_host=192.168.1.20 ansible_user=ubuntu

# Ad-hoc commands
ansible all -i hosts.ini -m ping                                    # Ping all hosts
ansible webservers -i hosts.ini -m command -a "uptime"              # Run command
ansible all -i hosts.ini -m apt -a "name=nginx state=present" -b    # Install package
ansible all -i hosts.ini -m service -a "name=nginx state=started" -b # Start service
ansible all -i hosts.ini -m copy -a "src=./file dest=/tmp/file"    # Copy file

# Playbook (deploy.yml)
# ---
# - hosts: webservers
#   become: yes
#   tasks:
#     - name: Install Nginx
#       apt: name=nginx state=present
#     - name: Start Nginx
#       service: name=nginx state=started enabled=yes
#     - name: Copy config
#       template: src=nginx.conf.j2 dest=/etc/nginx/nginx.conf
#       notify: restart nginx
#   handlers:
#     - name: restart nginx
#       service: name=nginx state=restarted

ansible-playbook -i hosts.ini deploy.yml                             # Run playbook
ansible-playbook -i hosts.ini deploy.yml --check                     # Dry run
ansible-playbook -i hosts.ini deploy.yml --syntax-check              # Check syntax
```

---

### Kubernetes `kubectl` Basics
```bash
# Context & Cluster
kubectl cluster-info                          # Cluster info
kubectl get nodes                             # List nodes
kubectl config get-contexts                   # List contexts
kubectl config use-context prod-cluster       # Switch context

# Pods
kubectl get pods                              # List pods
kubectl get pods -o wide                      # Pods with IP/node details
kubectl get pods --all-namespaces             # Pods across all namespaces
kubectl describe pod my-pod                   # Pod details
kubectl logs -f pod-name                      # Follow pod logs
kubectl exec -it pod-name -- /bin/bash        # Shell into pod

# Deployments
kubectl get deployments                       # List deployments
kubectl create deployment nginx --image=nginx:alpine  # Create deployment
kubectl scale deployment nginx --replicas=3   # Scale to 3 replicas
kubectl set image deployment/nginx nginx=nginx:1.25  # Rolling update
kubectl rollout undo deployment/nginx         # Rollback

# Services
kubectl expose deployment nginx --port=80 --type=LoadBalancer  # Expose as service
kubectl get svc                               # List services
kubectl port-forward svc/nginx 8080:80        # Port forward to service

# Config & Secrets
kubectl create configmap app-config --from-file=config.properties
kubectl create secret generic db-secret --from-literal=password=mypass
```

---

### Git Shortcuts (DevOps Daily)
```bash
git log --oneline --graph --all               # Visual commit history
git stash && git pull && git stash pop        # Pull with local changes
git reset --soft HEAD~1                       # Undo last commit (keep changes)
git reset --hard HEAD~1                       # Undo last commit (discard changes)
git revert HEAD                               # Safe undo (creates new commit)
git branch -d old-branch                      # Delete local branch
git push origin --delete old-branch           # Delete remote branch
git tag v1.0.0 && git push --tags             # Create and push tag
git cherry-pick commit-hash                   # Apply specific commit to current branch
git diff --cached                             # Show staged changes
```

---

### Common DevOps Ports Reference

| Port | Protocol | Service |
|------|----------|---------|
| 22 | TCP | SSH |
| 80 | TCP | HTTP |
| 443 | TCP | HTTPS |
| 3306 | TCP | MySQL/MariaDB |
| 5432 | TCP | PostgreSQL |
| 6379 | TCP | Redis |
| 27017 | TCP | MongoDB |
| 8080 | TCP | HTTP Alternate (Tomcat, Jenkins) |
| 8443 | TCP | HTTPS Alternate |
| 9090 | TCP | Prometheus, Cockpit |
| 3000 | TCP | Grafana, Node.js apps |
| 5000 | TCP | Flask, Docker registry |
| 2375 | TCP | Docker (unencrypted) |
| 2376 | TCP | Docker (TLS) |
| 6443 | TCP | Kubernetes API |
| 10250 | TCP | Kubelet API |
| 3000-10000 | TCP | NodePort range (K8s) |

---

### System Recovery & Rescue

#### Boot into Rescue Mode
```bash
# At GRUB menu: press 'e' to edit boot params
# Add to linux line: single or init=/bin/bash
# Then remount root as read/write:
mount -o remount,rw /
```

#### Reset Root Password
```bash
# Boot into recovery/single mode
passwd root                                  # Set new root password
```

#### Filesystem Check
```bash
sudo fsck /dev/sda1                          # Check filesystem (unmount first!)
sudo fsck -y /dev/sda1                       # Auto-repair
sudo fsck -f /dev/sda1                       # Force check even if clean
sudo tune2fs -l /dev/sda1 | grep -i "mount count\|check"  # Check interval info
```

---

## Shell Scripting - Quick Reference (Bash Modern Style)

---

### Script Structure & Shebang
```bash
#!/bin/bash
set -euo pipefail          # Exit on error, undefined var, pipe fail
# OR individually:
set -e                     # Exit on any error
set -u                     # Treat unset variables as error
set -o pipefail            # Pipeline fails if any command fails
set -x                     # Debug mode (print each command before execution)
```

---

### Variables

#### Assignment & Expansion
```bash
name="Arvind"                              # No spaces around =
readonly pi=3.14159                         # Read-only constant
local var="scope"                           # Local variable (inside function)

echo "$name"                               # Always quote variables
echo "${name}_suffix"                      # Brace to delimit
echo "${#name}"                            # String length → 6
echo "${name:0:3}"                         # Substring → Arv
echo "${name,,}"                           # Lowercase → arvind
echo "${name^^}"                           # Uppercase → ARVIND
```

#### Default Values
```bash
echo "${var:-default}"                     # Use default if var is unset/null
echo "${var:=default}"                     # Assign default if unset/null
echo "${var:?error msg}"                   # Exit with error if unset/null
echo "${var:+alternate}"                   # Use alternate if var is set
```

#### Indirection & Replacement
```bash
varname="USER"
echo "${!varname}"                         # Indirect reference → arvind

file="photo.jpg"
echo "${file%.jpg}"                        # Remove suffix → photo
echo "${file%.*}"                          # Remove shortest suffix → photo
echo "${file%%.*}"                         # Remove longest suffix → photo
echo "${file#photo}"                       # Remove prefix → .jpg
echo "${file/#photo/image}"                # Replace prefix → image.jpg
echo "${file/%jpg/png}"                    # Replace suffix → photo.png
echo "${file/jpg/png}"                     # First match replace
echo "${file//j/J}"                        # Replace all matches → photo.Jpg
```

---

### Arrays
```bash
# Indexed Array
fruits=("apple" "banana" "cherry")
echo "${fruits[0]}"                        # First element → apple
echo "${fruits[@]}"                        # All elements
echo "${#fruits[@]}"                       # Array length → 3
echo "${!fruits[@]}"                       # All indices → 0 1 2
fruits+=("date")                           # Append element

# Associative Array (Bash 4+)
declare -A user
user=( [name]="Arvind" [age]=30 [city]="Delhi" )
echo "${user[name]}"                       # → Arvind
echo "${!user[@]}"                         # All keys → name age city
echo "${user[@]}"                          # All values
```

---

### Arithmetic Operations
```bash
# $(( )) - Modern style (no expr needed)
a=10; b=3
echo $((a + b))                            # Addition → 13
echo $((a - b))                            # Subtraction → 7
echo $((a * b))                            # Multiplication → 30
echo $((a / b))                            # Division → 3
echo $((a % b))                            # Modulus → 1
echo $((a ** b))                           # Exponentiation → 1000
echo $((++a))                              # Pre-increment
echo $((b--))                              # Post-decrement

# let - Alternative
let "result = a * 5 + 2"
echo "$(( RANDOM % 100 ))"                 # Random 0-99
```

---

### String Operations
```bash
# Comparison
[[ "$str1" == "$str2" ]]                   # Equal (pattern matching)
[[ "$str1" != "$str2" ]]                   # Not equal
[[ "$str1" =~ ^Hello ]]                    # Regex match
[[ -z "$str" ]]                            # Empty string (zero length)
[[ -n "$str" ]]                            # Non-empty string

# Concatenation
greeting="Hello, " "$name" "!"            # Hello, Arvind!

# Length
echo "${#str}"                             # String length

# Case Conversion (Bash 4+)
echo "${str^}"                             # Capitalize first
echo "${str^^}"                            # All uppercase
echo "${str,}"                             # Lowercase first
echo "${str,,}"                            # All lowercase
```

---

### Conditional Statements

#### `if` - Modern `[[ ]]` Style
```bash
# Numeric comparison (inside (( )) or with -eq)
if (( a > b )); then
    echo "a is greater"
elif (( a == b )); then
    echo "equal"
else
    echo "a is less"
fi

# String comparison
if [[ "$name" == "Arvind" ]]; then
    echo "Match"
fi

# File conditions
if [[ -f "$file" ]]; then                  # File exists (regular file)
    echo "File exists"
fi
if [[ -d "$dir" ]]; then                   # Directory exists
    echo "Is directory"
fi
if [[ -e "$path" ]]; then                  # Path exists (any type)
    echo "Exists"
fi
if [[ -r "$file" && -w "$file" ]]; then    # Readable AND writable
    echo "Read+Write"
fi
if [[ -x "$file" || -d "$file" ]]; then    # Executable OR directory
    echo "Exec or Dir"
fi
if [[ ! -z "$var" ]]; then                 # NOT empty
    echo "Not empty"
fi
if [[ -s "$file" ]]; then                  # File exists AND size > 0
    echo "Not empty file"
fi
if [[ "$FILE" -nt "$OTHER" ]]; then        # NEWER Than
    echo "File is newer"
fi
```

#### `case` Statement
```bash
case "$input" in
    start|begin)
        echo "Starting..."
        ;;
    stop|end)
        echo "Stopping..."
        ;;
    restart)
        echo "Restarting..."
        ;;
    [0-9]*)
        echo "Starts with digit"
        ;;
    *.txt|*.md)
        echo "Text or markdown file"
        ;;
    "")
        echo "Empty input"
        ;;
    *)
        echo "Unknown option: $input"
        exit 1
        ;;
esac
```

#### Ternary-like (one-liner condition)
```bash
[[ "$age" -ge 18 ]] && echo "Adult" || echo "Minor"
result=$(( a > b ? a : b ))                # Ternary: max of a,b
```

---

### File Test Operators

| Operator | True if |
|----------|---------|
| `-e` | Path exists |
| `-f` | Regular file |
| `-d` | Directory |
| `-L` | Symbolic link |
| `-r` | Readable |
| `-w` | Writable |
| `-x` | Executable |
| `-s` | Size > 0 |
| `-N` | Modified since last read |
| `-nt` | Newer than (file1 -nt file2) |
| `-ot` | Older than |
| `-O` | Owned by current user |
| `-G` | Group-owned by current user |

---

### Loops

#### `for` Loop (Multiple Styles)
```bash
# C-style (indexed)
for (( i=0; i<5; i++ )); do
    echo "Iteration $i"
done

# Range
for i in {1..5}; do
    echo "Number $i"
done

# Range with step
for i in {0..10..2}; do                    # 0 2 4 6 8 10
    echo "Even $i"
done

# List/array iteration
for fruit in "${fruits[@]}"; do
    echo "Fruit: $fruit"
done

# Command output
for file in /var/log/*.log; do
    echo "Log: $file"
done

# Associative array
for key in "${!user[@]}"; do
    echo "$key → ${user[$key]}"
done

# Positional parameters
for arg in "$@"; do
    echo "Argument: $arg"
done

# With break/continue
for i in {1..10}; do
    (( i % 2 == 0 )) && continue           # Skip evens
    (( i > 7 )) && break                    # Stop after 7
    echo "Odd under 8: $i"
done
```

#### `while` Loop
```bash
# Counter
count=0
while (( count < 5 )); do
    echo "Count: $count"
    ((count++))
done

# Read file line by line
while IFS= read -r line; do
    echo "Line: $line"
done < "input.txt"

# Read CSV
while IFS=',' read -r col1 col2 col3; do
    echo "Col1: $col1, Col2: $col2"
done < "data.csv"

# Infinite loop (with break condition)
while true; do
    read -p "Enter command: " cmd
    [[ "$cmd" == "quit" ]] && break
    eval "$cmd"
done

# Process substitution
while read -r process; do
    echo "Running: $process"
done < <(ps aux | grep python)

# Watch until condition
while ! ping -c1 google.com &>/dev/null; do
    echo "Waiting for network..."
    sleep 2
done
echo "Network is up!"
```

#### `until` Loop (Opposite of while)
```bash
count=0
until (( count >= 5 )); do                 # Runs until condition is true
    echo "Count: $count"
    ((count++))
done
```

---

### Functions

```bash
# Define
greet() {
    local name="$1"                        # First argument
    local age="${2:-30}"                   # Second arg with default
    echo "Hello $name ($age)"
}

# Call
greet "Arvind" 25

# Return value (0-255, 0=success)
is_even() {
    (( $1 % 2 == 0 )) && return 0 || return 1
}
if is_even 4; then
    echo "Even"
fi

# Return string (use echo & capture)
get_date() {
    echo "$(date +%Y-%m-%d)"
}
today=$(get_date)
echo "Today: $today"

# Function with local variables
calculate() {
    local a=$1 b=$2 op=$3
    case $op in
        +) echo $((a + b)) ;;
        -) echo $((a - b)) ;;
        *) echo "Invalid op" >&2; return 1 ;;
    esac
}

# Export function (accessible in subshells)
export -f greet
```

---

### Input / Output

#### `read` - User Input
```bash
read -p "Enter name: " name                # Prompt + input
read -s -p "Password: " pass               # Silent (no echo)
echo                                       # Newline after silent input
read -t 5 -p "Quick (5s): " input          # Timeout
read -n1 -p "Press any key: " key          # Single character
read -a arr -p "Enter numbers: "           # Read into array → ${arr[0]}
IFS=',' read -r f1 f2 f3 <<< "a,b,c"       # Here-string to variables
```

#### `select` - Menu
```bash
PS3="Choose option: "                      # Custom prompt
options=("Start" "Stop" "Restart" "Quit")
select opt in "${options[@]}"; do
    case $opt in
        Start)   echo "Starting..." ;;
        Stop)    echo "Stopping..." ;;
        Restart) echo "Restarting..." ;;
        Quit)    break ;;
        *)       echo "Invalid" ;;
    esac
done
```

---

### Exit Codes & Error Handling

```bash
# Exit codes: 0=success, 1-255=error
command_success && echo "OK" || echo "FAIL"

# Trap errors
trap 'echo "Error on line $LINENO"; exit 1' ERR

# Trap EXIT (always runs)
trap 'cleanup_temp_files' EXIT

# Custom exit
if [[ ! -f "$config" ]]; then
    echo "Config not found" >&2            # stderr
    exit 1
fi

# Last exit code
mycmd
echo "Exit code: $?"
```

---

### Command Substitution
```bash
# Modern $() (preferred over backticks ` `)
current_dir=$(pwd)
files_count=$(ls -1 | wc -l)
ip=$(curl -s ifconfig.me)

# Nested substitution
result=$(echo "Today is $(date +%A)")
```

---

### Process Substitution
```bash
# Compare two command outputs
diff <(ls /dir1) <(ls /dir2)

# Read from both simultaneously
while IFS= read -r line1 && IFS= read -r line2 <&3; do
    echo "File1: $line1, File2: $line2"
done < file1 3< file2

# Pass to function
wc -l <(cat *.log)                         # Count lines from process output
```

---

### Here Documents & Strings
```bash
# Here Document (<<)
cat << 'EOF' > output.txt                   # Quotes prevent variable expansion
Hello $USER
This is literal text
EOF

# Here String (<<<)
grep "error" <<< "$log_data"

# Multi-line variable assignment
sql=$(cat <<-SQL                           # Tab-indented (<<-)
    SELECT * FROM users
    WHERE active = 1
SQL
)
```

---

### Useful Built-in Variables

| Variable | Description |
|----------|-------------|
| `$0` | Script name |
| `$1, $2, ...` | Positional arguments |
| `$#` | Number of arguments |
| `$@` | All arguments (quoted individually) |
| `$*` | All arguments (single string) |
| `$?` | Last exit code |
| `$$` | Current script PID |
| `$!` | Last background PID |
| `$-` | Current shell flags |
| `$_` | Last argument of previous command |
| `LINENO` | Current line number in script |
| `RANDOM` | Random number (0-32767) |
| `SECONDS` | Script running time (seconds) |
| `BASH_VERSION` | Bash version string |
| `HOSTNAME` | System hostname |
| `IFS` | Internal field separator (default: space/tab/newline) |

---

### Arrays - Advanced Operations

```bash
# Indexed array operations
arr=()
arr+=(1 2 3)                               # Append multiple
arr=( "${arr[@]:1}" )                      # Remove first element
arr=( "${arr[@]:0:2}" )                     # Keep first 2 elements

# Joining array into string
IFS=','; echo "${arr[*]}"; unset IFS       # → 1,2,3

# Array from command
mapfile -t lines < <(cat file.txt)         # Read lines into array
```

---

### Globbing & Pattern Matching

```bash
shopt -s extglob                            # Enable extended patterns
shopt -s globstar                          # ** matches recursively

# Extended patterns
if [[ "$file" = @(*.txt|*.md) ]]; then     # @(pattern1|pattern2)
    echo "Text file"
fi

# Globstar for recursive find
for file in **/*.log; do                    # All .log recursively
    echo "$file"
done

# Nullglob (avoid literal * if no match)
shopt -s nullglob
for file in *.nonexistent; do              # Loop zero times instead of literal
    echo "$file"
done
```

---

### Common One-Liner Patterns

```bash
# Iterate and rename
for f in *.jpg; do mv "$f" "${f%.jpg}.png"; done

# Count occurrences
grep -c "ERROR" app.log

# Backup with timestamp
cp file.conf{,.$(date +%Y%m%d_%H%M%S).bak}

# Kill all matching processes
pkill -f "python server.py"

# Watch disk usage
watch -n5 'df -h / | tail -1'

# Find and replace across files
sed -i 's/oldhost/newhost/g' config/*.yml

# Extract compressed archive by extension
extract() { case "$1" in *.tar.gz|*.tgz) tar xzf "$1";; *.zip) unzip "$1";; *.rar) unrar x "$1";; esac; }

# Retry command until success
until cmd; do sleep 1; done

# Measure execution time
time myscript.sh

# Parallel execution in background
for url in "${urls[@]}"; do (curl -O "$url" &); done; wait
```

---

### Associative Array - Real Example (Config Parser)
```bash
# Parse key=value config file
declare -A config
while IFS='=' read -r key val; do
    # Skip comments and empty lines
    [[ "$key" =~ ^[[:space:]]*# || -z "$key" ]] && continue
    config["$key"]="$val"
done < "app.conf"

echo "DB_HOST = ${config[DB_HOST]}"
echo "DB_PORT = ${config[DB_PORT]}"
```

---

### Signal Handling
```bash
# Trap signals for cleanup
cleanup() {
    echo "Cleaning up..."
    rm -f /tmp/lockfile
    exit 0
}
trap cleanup SIGINT SIGTERM EXIT

# Ignore signal
trap '' SIGINT                               # Ignore Ctrl+C

# Timeout a command
timeout 5 sleep 10 || echo "Timed out"
```

---

### Debugging Techniques
```bash
bash -n script.sh                            # Syntax check (no execution)
bash -x script.sh                            # Trace execution (print commands)
bash -v script.sh                            # Print input lines
set -x                                       # Debug block start
# code to debug ...
set +x                                       # Debug block end

# PS4 - custom debug prompt
export PS4='+(${BASH_SOURCE}:${LINENO}): ${FUNCNAME[0]:+${FUNCNAME[0]}(): }'
set -x
# Now debug output shows file, line, function name
```
---

## Troubleshooting & Incident Handling

---

### Common Log File Locations

| Service/App | Log Path | Purpose |
|-------------|----------|---------|
| **System** | `/var/log/syslog` | General system messages |
| **Auth** | `/var/log/auth.log` | SSH logins, sudo, auth failures |
| **Kernel** | `/var/log/kern.log` | Kernel messages, hardware errors |
| **dmesg** | `dmesg` command | Kernel ring buffer (boot messages) |
| **Nginx** | `/var/log/nginx/access.log` | HTTP request log |
| **Nginx** | `/var/log/nginx/error.log` | Nginx errors (config, upstream fails) |
| **Apache** | `/var/log/apache2/access.log` | HTTP request log |
| **Apache** | `/var/log/apache2/error.log` | Apache errors |
| **Tomcat** | `/var/log/tomcat*/catalina.out` | Main Tomcat log (stdout) |
| **Tomcat** | `/var/log/tomcat*/localhost.log` | App-specific error log |
| **Tomcat** | `/var/log/tomcat*/manager.log` | Manager app logs |
| **MySQL/MariaDB** | `/var/log/mysql/error.log` | DB connection/query errors |
| **PostgreSQL** | `/var/log/postgresql/postgresql-*.log` | PG errors, connections |
| **Docker** | `docker logs <container>` | Container stdout/stderr |
| **Docker** | `/var/lib/docker/containers/<id>/<id>-json.log` | Raw container logs |
| **Systemd** | `journalctl -u <service>` | Service journal logs |
| **SSH** | `/var/log/auth.log` | SSH auth attempts |
| **Cron** | `journalctl -u cron` | Cron job execution logs |
| **Redis** | `/var/log/redis/redis-server.log` | Redis errors, snapshots |
| **Jenkins** | `/var/log/jenkins/jenkins.log` | Jenkins build/plugin logs |
| **Kubernetes** | `kubectl logs <pod>` | Pod container logs |
| **Kubernetes** | `/var/log/pods/` | Node-level pod logs |
| **Nginx Unit** | `/var/log/unit.log` | Unit application server logs |

---

### Quick Log Investigation Patterns

#### Check what failed recently
```bash
# Last 50 errors (case-insensitive)
grep -i "error" /var/log/nginx/error.log | tail -50

# Errors in last N minutes
journalctl -u nginx --since "10 min ago"

# Count errors by hour
grep -c "$(date +%Y-%m-%dT%H)" /var/log/syslog

# Show context around error (5 lines before/after)
grep -B5 -A5 "FATAL" /var/log/tomcat/catalina.out
```

#### Real-time monitoring
```bash
# Follow log live
tail -f /var/log/nginx/error.log

# Follow with grep filter
tail -f /var/log/syslog | grep -i "error"

# systemd journal follow
journalctl -u nginx -f

# Multiple logs at once
tail -f /var/log/nginx/*.log

# With timestamp
tail -f /var/log/syslog | while read line; do echo "$(date '+%H:%M:%S') $line"; done
```

---

### Nginx Troubleshooting

```bash
# Config test (always check before reload)
nginx -t                                    # Test config syntax
nginx -T                                    # Test + dump full config

# Reload without downtime
nginx -s reload

# Check if process is running
pgrep -a nginx

# Check listening port
ss -tlnp | grep nginx

# Common errors:
# "connection refused" → nginx not running or wrong port
# "502 Bad Gateway"   → upstream (app server) down
# "404 Not Found"     → missing root or wrong location
# "Permission denied" → selinux or file permissions

# Check upstream (if proxying)
curl -I http://localhost:8080/health        # Test backend directly
curl -I http://localhost:80                 # Test nginx response

# Access log analysis
awk '{print $1}' /var/log/nginx/access.log | sort | uniq -c | sort -rn | head -10   # Top IPs
awk '{print $9}' /var/log/nginx/access.log | sort | uniq -c | sort -rn              # Status codes
awk '{print $7}' /var/log/nginx/access.log | sort | uniq -c | sort -rn | head -10   # Top URLs

# Find 5xx errors
grep 'HTTP/1.[01]" 5[0-9][0-9]' /var/log/nginx/access.log
```

---

### Apache Troubleshooting

```bash
# Config test
apache2ctl configtest                       # or httpd -t

# Graceful restart
apache2ctl graceful

# Check modules loaded
apache2ctl -M

# Virtual hosts
apache2ctl -S                               # Show all vhosts

# Common error patterns
grep "DH key too small" /var/log/apache2/error.log    # SSL config issue
grep "client denied by server configuration" error.log # Permission issue
```

---

### Tomcat Troubleshooting

```bash
# Log locations
TOMCAT_HOME=/var/lib/tomcat10
$TOMCAT_HOME/logs/catalina.out              # Main log (stdout/stderr)
$TOMCAT_HOME/logs/localhost.log             # App errors
$TOMCAT_HOME/logs/manager.log               # Manager app
$TOMCAT_HOME/logs/host-manager.log          # Virtual host

# Check if Tomcat is running
ps aux | grep tomcat
ss -tlnp | grep java                        # Typically on 8080

# Heap dump / OutOfMemoryError
grep "OutOfMemoryError" /var/log/tomcat/catalina.out
grep "java.lang.OutOfMemoryError" /var/log/tomcat/catalina.out

# Thread dump (for hang/deadlock)
kill -3 $(pgrep -f "catalina")              # Send SIGQUIT → dump in catalina.out
jstack -l <pid>                             # Alternative thread dump

# Check deployed apps
curl -u admin:password http://localhost:8080/manager/text/list

# Common deployment issues
grep "FAIL" /var/log/tomcat/catalina.out
grep "ClassNotFoundException" /var/log/tomcat/localhost.log
grep "NoClassDefFoundError" /var/log/tomcat/localhost.log
grep "Context" /var/log/tomcat/catalina.out | grep -i "start\|stop\|fail"
```

---

### MySQL/MariaDB Troubleshooting

```bash
# Check status
systemctl status mysql
mysqladmin -u root -p ping                  # Check if server is alive
mysqladmin -u root -p status                # Uptime, threads, queries

# Logs
/var/log/mysql/error.log                    # Error log
grep "Access denied" /var/log/mysql/error.log
grep "Can't connect" /var/log/mysql/error.log

# Process list
mysql -u root -p -e "SHOW FULL PROCESSLIST\G"   # Find slow/locked queries
mysql -u root -p -e "SHOW ENGINE INNODB STATUS\G" # InnoDB deadlocks

# Slow query log
mysql -u root -p -e "SET GLOBAL slow_query_log = ON;"
mysql -u root -p -e "SET GLOBAL long_query_time = 2;" # Log queries > 2s
tail -f /var/log/mysql/mysql-slow.log

# Common issues
# "Table is marked as crashed" → mysqlcheck -r <db> <table>
# "Too many connections"      → Increase max_connections in my.cnf
# "Disk full"                 → Clean binary logs: PURGE BINARY LOGS BEFORE NOW();

# Repair crashed table
mysqlcheck -u root -p --auto-repair --all-databases

# Binary logs (space cleanup)
mysql -u root -p -e "PURGE BINARY LOGS BEFORE NOW();"
mysql -u root -p -e "RESET MASTER;"        # Remove all binlogs (CAUTION)
```

---

### PostgreSQL Troubleshooting

```bash
# Check status
systemctl status postgresql
pg_isready                                  # Check connection status

# Logs
tail -f /var/log/postgresql/postgresql-*-main.log
grep "FATAL" /var/log/postgresql/postgresql-*.log
grep "could not connect" /var/log/postgresql/postgresql-*.log

# Active connections
psql -c "SELECT * FROM pg_stat_activity WHERE state = 'active';"

# Kill hanging queries
psql -c "SELECT pg_terminate_backend(pid) FROM pg_stat_activity WHERE state = 'active' AND pid <> pg_backend_pid();"

# Find slow queries (enable in postgresql.conf: log_min_duration_statement = 2000)
grep "duration:" /var/log/postgresql/postgresql-*.log

# Table bloat / vacuum
psql -c "SELECT schemaname, tablename, n_dead_tup FROM pg_stat_user_tables WHERE n_dead_tup > 1000 ORDER BY n_dead_tup DESC;"
psql -c "VACUUM ANALYZE;"                  # Reclaim storage, update stats
psql -c "VACUUM FULL;"                     # Full reclaim (locks table)
```

---

### Docker Troubleshooting

```bash
# Container logs
docker logs <container>                     # Full log
docker logs --tail 100 <container>          # Last 100 lines
docker logs -f <container>                  # Follow mode
docker logs --since 5m <container>          # Last 5 minutes

# Inspect container
docker inspect <container>                  # Full JSON (mounts, network, env)
docker inspect --format '{{.State.Running}}' <container>  # Quick format

# Resource usage
docker stats                                # Live CPU/memory/network per container

# Entrypoint/command issues
docker run -it --entrypoint sh <image>      # Override entrypoint for debug

# Network issues
docker network ls
docker network inspect bridge
docker exec <container> ping google.com     # Check connectivity inside

# Volume/mount issues
docker inspect -f '{{json .Mounts}}' <container> | jq .

# Common scenarios:
# "Container exits immediately" → docker logs <container> to see error
# "Port already allocated"     → ss -tlnp | grep <port> to find process
# "No space left on device"    → docker system prune -a
# "Image pull failed"          → check DNS: dig registry-1.docker.io

# Disk cleanup
docker system df                           # Show disk usage
docker system prune -a --volumes           # Remove ALL unused containers/images/volumes
docker volume prune                        # Remove dangling volumes
```

---

### Kubernetes Troubleshooting

```bash
# Pod status
kubectl get pods -o wide                   # All pods with node/IP
kubectl describe pod <pod>                  # Events, conditions, container states

# Container logs
kubectl logs <pod>                          # Container logs
kubectl logs --tail=50 -f <pod>            # Last 50 + follow
kubectl logs <pod> -c <container>          # Multi-container pod
kubectl logs --previous <pod>              # Last terminated container logs

# Debug with ephemeral container
kubectl debug -it <pod> --image=nicolaka/netshoot:latest -- /bin/bash

# Events
kubectl get events --sort-by='.lastTimestamp'   # Cluster events (most common debugging start)
kubectl get events --field-selector involvedObject.kind=Pod

# Node issues
kubectl describe node <node>
kubectl top node                            # Node resource usage
kubectl top pod                             # Pod resource usage

# CrashLoopBackOff
kubectl logs <pod> --previous               # See why pod crashed
kubectl describe pod <pod> | grep -A10 "Last State"

# ImagePullBackOff
kubectl describe pod <pod> | grep -A5 "Failed"
# Check image name, tag, registry credentials

# Pending pod (not scheduled)
kubectl describe pod <pod> | grep -A5 "Events"
# Usually: insufficient CPU/memory, PVC not bound, taints

# Service/DNS issues
kubectl run debug --image=nicolaka/netshoot -it --rm -- /bin/bash
# Inside: nslookup service-name, curl http://service-name:port

# PVC issues
kubectl describe pvc <pvc-name>             # Check bound status, events
kubectl get pv                              # Available persistent volumes

# Network policy blocking
kubectl get networkpolicies                # List network policies
kubectl describe networkpolicy <name>       # Check ingress/egress rules
```

---

### Jenkins Troubleshooting

```bash
# Logs
/var/log/jenkins/jenkins.log               # Main log
journalctl -u jenkins -f                    # Systemd journal

# Check if running
systemctl status jenkins
ss -tlnp | grep 8080                        # Default port

# Common issues & fixes

# 1. "Jenkins is down / unreachable"
systemctl restart jenkins
journalctl -u jenkins --since "1 hour ago" | grep -i "error\|exception\|failed"

# 2. "Disk full" (Jenkins builds consume space)
du -sh /var/lib/jenkins/jobs/* | sort -rh | head -10    # Largest jobs
du -sh /var/lib/jenkins/workspace/* | sort -rh | head -10
du -sh /var/lib/jenkins/logs/

# Clean old builds
# Jenkins → Manage Jenkins → Script Console
# Jenkins.instance.getAllItems(Job.class).each { job ->
#   job.getBuilds().each { build ->
#     if(build.getNumber() < 10) build.delete()
#   }
# }

# 3. "Plugin installation failed"
grep "Plugin" /var/log/jenkins/jenkins.log | tail -20

# 4. "Scriptler / credential errors"
ls -la /var/lib/jenkins/credentials.xml     # Check permissions
ls -la /var/lib/jenkins/secrets/            # Check master key
```

---

### Redis Troubleshooting

```bash
# Check status
systemctl status redis
redis-cli ping                              # Should return PONG

# Logs
tail -f /var/log/redis/redis-server.log

# Common issues
redis-cli INFO                              # Server stats overview
redis-cli INFO keyspace                     # Key counts per DB
redis-cli CLIENT LIST                       # Active connections
redis-cli SLOWLOG GET 10                    # Last 10 slow queries
redis-cli MEMORY STATS                      # Memory breakdown
redis-cli MONITOR                           # Watch all commands live (CAUTION: high load)

# OutOfMemory / evictions
redis-cli INFO | grep evicted_keys          # Keys evicted (too much memory)
redis-cli CONFIG SET maxmemory 2gb          # Increase max memory
redis-cli CONFIG SET maxmemory-policy allkeys-lru  # Change eviction policy

# Latency issues
redis-cli --latency                         # Real-time latency test
redis-cli --latency-history -i 1           # Every 1 second
redis-cli --bigkeys                         # Find large keys (slow scan)
```

---

### SSH Troubleshooting

```bash
# Verbose mode (for connection issues)
ssh -vvv user@host                         # Debug connection

# Check SSH daemon status
systemctl status sshd
ss -tlnp | grep :22

# Logs
grep "sshd" /var/log/auth.log | tail -50
journalctl -u sshd -f

# Permission errors (most common)
chmod 600 ~/.ssh/id_rsa                    # Private key must be 600
chmod 644 ~/.ssh/id_rsa.pub                # Public key must be 644
chmod 700 ~/.ssh                            # .ssh dir must be 700
chmod 755 ~                                 # Home dir should NOT be writable by group

# Known hosts issues
ssh-keygen -R hostname                     # Remove host from known_hosts
ssh -o StrictHostKeyChecking=no user@host  # Skip host key check (temporary)

# Authentication failures
grep "Failed password" /var/log/auth.log | tail -10
grep "Authentication refused" /var/log/auth.log

# Connection refused / timeout
nc -zv host 22                             # Check if port 22 is open
telnet host 22                             # Alternative
traceroute host                            # Network path check
```

---

### System Resource Troubleshooting

#### High CPU
```bash
# Find the culprit
top -bn1 | head -20                        # Top CPU processes
ps aux --sort=-%cpu | head -10             # Top 10 CPU consumers
mpstat -P ALL 1 5                          # Per-core CPU breakdown

# Thread-level analysis
top -H -p <pid>                            # Show threads of a process
strace -p <pid> -c                         # Syscall summary for process
```

#### High Memory
```bash
free -h                                    # Memory overview
ps aux --sort=-%mem | head -10             # Top 10 memory consumers
cat /proc/meminfo                          # Detailed memory info
vmstat -s                                  # Memory event counters

# Swap usage
swapon --show                              # Swap status
vmstat 1 5                                 # Check si/so (swap in/out) columns
```

#### Disk Full
```bash
df -h                                      # Disk usage overview
du -sh /* | sort -rh | head -10           # Top-level largest directories
du -sh /var/log/* | sort -rh | head -10   # Large log files
find / -type f -size +500M -exec ls -lh {} \; 2>/dev/null  # Files >500MB

# Find and clean large log files
find /var/log -name "*.log" -size +100M -exec truncate -s 0 {} \;  # WARNING: irreversibly empties logs

# Open file descriptors (too many open files)
lsof | wc -l                               # Total open files
lsof -u www-data | wc -l                   # Open files by user
cat /proc/sys/fs/file-max                  # System max file limit
ulimit -n                                  # Per-process limit
```

#### Network Issues
```bash
# General connectivity
ping -c4 8.8.8.8                           # Internet reachable?
curl -I https://example.com                # HTTP reachable?

# DNS issues
dig google.com +short                      # DNS resolving?
cat /etc/resolv.conf                       # DNS config

# Port in use?
ss -tulpn | grep :80                       # What's listening on port 80
lsof -i :8080                              # Process using port 8080

# Packet loss / latency
mtr google.com                             # Path analysis
ping -c 100 -i 0.2 google.com | grep -E "loss|avg"  # Packet loss %

# Bandwidth
iftop                                      # Real-time bandwidth (install first)
nload                                      # Per-interface bandwidth
```

#### Service Won't Start
```bash
# Step-by-step diagnostic
systemctl status myservice                # Status + last log lines
journalctl -u myservice -x --since "5 min ago"  # Full log with explanations
journalctl -u myservice -n 50             # Last 50 lines

# Check syntax (most services)
nginx -t                                   # Nginx config test
apache2ctl configtest                      # Apache config test
sshd -t                                    # SSH config test

# Check port conflict
ss -tulpn | grep :<port>

# Permission errors
ls -la /etc/myservice/                     # Check config perms
ls -la /var/log/myservice/                 # Check log dir perms
journalctl -u myservice | grep -i "permission denied"

# Dependency check
systemctl list-dependencies myservice      # What it depends on
systemctl status $(systemctl list-dependencies myservice | grep .service)
```

---

### Quick Incident Response Checklist

```text
1. IS THE SERVICE RUNNING?
   systemctl status <service>
   ps aux | grep <service>

2. IS THE PORT OPEN?
   ss -tulpn | grep <port>
   curl -I http://localhost:<port>

3. WHAT DO THE LOGS SAY?
   tail -100 /var/log/<service>/error.log
   journalctl -u <service> -n 50 --no-pager

4. IS DISK FULL?
   df -h
   du -sh /var/log/

5. IS MEMORY FULL?
   free -h
   ps aux --sort=-%mem | head -5

6. IS CPU HIGH?
   top -bn1 | head -10
   ps aux --sort=-%cpu | head -5

7. IS NETWORK OK?
   ping -c3 <gateway>
   dig <hostname>

8. ARE PERMISSIONS CORRECT?
   ls -la /var/log/<service>/
   ls -la /etc/<service>/

9. CHECK RECENT CHANGES
   ls -lt /etc/<service>/ | head
   journalctl -u <service> --since "1 hour ago" | grep -i "error\|fail\|warn"

10. RESTART IF NEEDED
    sudo systemctl restart <service>
    sudo systemctl status <service> --no-pager
```

---

### Common Port & Service Quick Reference

| Port | Service | Check Command |
|------|---------|---------------|
| 22 | SSH | `ss -tlnp \| grep :22` |
| 80 | HTTP | `curl -I http://localhost` |
| 443 | HTTPS | `curl -I https://localhost -k` |
| 3306 | MySQL | `mysqladmin -u root -p ping` |
| 5432 | PostgreSQL | `pg_isready` |
| 6379 | Redis | `redis-cli ping` |
| 8080 | Tomcat/Jenkins | `curl -I http://localhost:8080` |
| 9090 | Prometheus | `curl http://localhost:9090/-/ready` |
| 3000 | Grafana | `curl -I http://localhost:3000` |
| 2375 | Docker | `curl http://localhost:2375/version` |
| 6443 | K8s API | `kubectl cluster-info` |
| 10250 | Kubelet | `curl -k https://localhost:10250/healthz` |

---

### Log Rotation & Management

```bash
# Check rotation config
cat /etc/logrotate.conf
cat /etc/logrotate.d/nginx

# Manually rotate
sudo logrotate -f /etc/logrotate.d/nginx

# Test rotation (dry-run)
sudo logrotate -d /etc/logrotate.d/nginx

# Check when logs were last rotated
ls -la /var/log/nginx/*.log*

# Compress old logs manually
gzip /var/log/nginx/access.log.1

# Truncate a log file (zero-size, no restart needed)
truncate -s 0 /var/log/nginx/error.log

# Avoid: rm + restart (causes log loss)
# Prefer: truncate or logrotate
```


### VI Editor/VIM/view

#### Command Description
```
vi filename - Creates a new file if it already does not exist, otherwise opens existing file.
vi -R filename - Opens an existing file in read only mode.
view filename - Opens an existing file in read only mode.
```
#### Cursor Options : Command Description
```
k - Moves the cursor up one line.
j - Moves the cursor down one line.
h - Moves the cursor to the left one character position.
l - Moves the cursor to the right one character position.
```

#### Editing Files Command Description
```
i - Inserts text before current cursor location.
I - Inserts text at beginning of current line.
a - Inserts text after current cursor location.
A - Inserts text at end of current line.
o - Creates a new line for text entry below cursor location.
O - Creates a new line for text entry above cursor location.
```

#### Deleting Characters Command Description
```
x - Deletes the character under the cursor location.
X - Deletes the character before the cursor location.
dw - Deletes from the current cursor location to the next word.
d^ - Deletes from current cursor position to the beginning of the line.
d$ - Deletes from current cursor position to the end of the line.
D - Deletes from the cursor position to the end of the current line.
dd - Deletes the line the cursor is on.
```
#### How to save file in vi …. Press (ESC + Shift + : ) Command Description
```
w - save and remain open like ctrl + s in windows
wq - save and quiet
x - save file and quiet editing mode
wq! - save and quiet forcefully
H - Go to start line
M - Go to Middle Line
L - Go to Last line
```
#### Some Options (file editing options are ) Command Description
```
r - Replace single character
R - Replace text from the cursor to right
s - substitute
g - globally
```
