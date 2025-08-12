# Basic Linux Commands 

```bash
>> pwd 

```

📌 Output example:

```
/c/Linux_Lab
```
## ls command

```bash
>> ls
```

📌 Output of ls:

```
  Desktop  Documents  Downloads  Music  Pictures  projects  Public  snap  Templates  Videos/
```

### ls flags

## ls command
The ls command is linux allows to to view all the files and folder in current working directory. Flag -a list down all file and folder including the one which are hidden

```bash
>> ls -la
```
📌 Output of ls - la:

```
total 112
drwxr-x--- 17 parth parth 4096 Aug 12 12:04 .
drwxr-xr-x  3 root  root  4096 Aug  6 22:17 ..
-rw-------  1 parth parth  706 Aug 11 09:13 .bash_history
-rw-r--r--  1 parth parth  220 Mar 31  2024 .bash_logout
-rw-r--r--  1 parth parth 3771 Mar 31  2024 .bashrc
drwx------ 14 parth parth 4096 Aug  7 11:39 .cache
-rw-rw-r--  1 parth parth    0 Aug 11 09:13 clanguage.c
-rw-rw-r--  1 parth parth    0 Aug 11 09:12 claungaunge.txt
drwxr-xr-x 13 parth parth 4096 Aug  7 10:35 .config
drwxr-xr-x  2 parth parth 4096 Aug  6 22:18 Desktop
drwxr-xr-x  2 parth parth 4096 Aug  6 22:18 Documents
drwxr-xr-x  2 parth parth 4096 Aug  6 22:18 Downloads
drwx------  2 parth parth 4096 Aug  6 22:26 .gnupg
drwx------  4 parth parth 4096 Aug  6 22:18 .local
drwxr-xr-x  2 parth parth 4096 Aug  6 22:18 Music
drwxr-xr-x  3 parth parth 4096 Aug  7 11:38 Pictures
-rw-r--r--  1 parth parth  807 Mar 31  2024 .profile
drwxrwxr-x  2 parth parth 4096 Aug  7 11:50 projects
drwxr-xr-x  2 parth parth 4096 Aug  6 22:18 Public
drwx------  4 parth parth 4096 Aug  6 22:40 snap
drwx------  2 parth parth 4096 Aug  6 22:18 .ssh
-rw-r--r--  1 parth parth    0 Aug  6 22:23 .sudo_as_admin_successful
drwxr-xr-x  2 parth parth 4096 Aug  6 22:18 Templates
-rw-r-----  1 parth parth    5 Aug 12 12:04 .vboxclient-clipboard-tty2-control.pid
-rw-r-----  1 parth parth    5 Aug 12 12:04 .vboxclient-clipboard-tty2-service.pid
-rw-r-----  1 parth parth    5 Aug 12 12:04 .vboxclient-draganddrop-tty2-control.pid
-rw-r-----  1 parth parth    5 Aug 12 12:04 .vboxclient-hostversion-tty2-control.pid
-rw-r-----  1 parth parth    5 Aug 12 12:04 .vboxclient-seamless-tty2-control.pid
-rw-r-----  1 parth parth    5 Aug 12 12:04 .vboxclient-vmsvga-session-tty2-control.pid
-rw-r-----  1 parth parth    5 Aug 12 12:04 .vboxclient-vmsvga-session-tty2-service.pid
drwxr-xr-x  2 parth parth 4096 Aug  6 22:18 Videos

```


