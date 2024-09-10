# Verify
- Difficulty: Easy
- Category: Forensics  
tags: `picoCTF 2024` `grep` `browser_webshell_solvable` `checksum`  
refer to [Source](https://play.picoctf.org/practice/challenge/450)

## Solution
``` shell
$ find ./files "*" -exec "./decrypt.sh" {} \; | grep "pico"
```
p.s. but it still show `bad magic number` for every file that isn't ans.
``` plain
picoCTF{trust_but_verify_87590c24}
```

### Improving
Learn how to use find command and grep more comprehensive.
