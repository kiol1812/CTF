# chrono
- Difficulty: Medium
- Category: `General Skills`  
- Date: 2024-09-22  
tags: `picoCTF 2023` `linux`  
refer to [Source](https://play.picoctf.org/practice/challenge/347?category=5&difficulty=2&page=1)

## Description
How to automate tasks to run at intervals on linux servers?
Use ssh to connect to this server:
Server: saturn.picoctf.net
Port: 53700
Username: picoplayer 
Password: emrdK96SGH

Entry server via ssh. and search "How to automate tasks to run at intervals on linux servers?" This is [result](https://www.geeksforgeeks.org/how-to-automate-tasks-with-cron-jobs-in-linux/) that i get. Seen like i must use cron to solve this problem.
## Solution
``` shell
$ssh -p 64240 picoplayer@saturn.picoctf.net
...
$ls
$cd /var/spool/cron/crontabs/
-bash: cd: /var/spool/cron/crontabs/: Permission denied
$crontab -e
...
$cat /etc/cron #tab tab
cron.d/       cron.daily/   cron.hourly/  cron.monthly/ cron.weekly/  crontab
$cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_0bb95b71}
```
``` plain
picoCTF{Sch3DUL7NG_T45K3_L1NUX_0bb95b71}
```

### Improving
