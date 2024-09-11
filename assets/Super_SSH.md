# Super SSH
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-11  
tags: `picoCTF 2024` `shell` `ssh` `browser_webshell_solvable`  
refer to [Source](https://play.picoctf.org/practice/challenge/424)

## Solution
ssh usage.
``` shell
$ssh -p {port} \<user>@{IP Address or Domain name}
```
``` shell
$ssh -p 50194 ctf-player@titan.picoctf.net
ctf-player@titan.picoctf.net's password:
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_3e293eea}
Connection to titan.picoctf.net closed.
```
``` plain
picoCTF{s3cur3_c0nn3ct10n_3e293eea}
```

### Improving