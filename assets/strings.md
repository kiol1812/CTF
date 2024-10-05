# strings
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-19  
tags: `picoCTF 2019`  
refer to [Source](https://play.picoctf.org/practice/challenge/37?page=5)

## Description
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings) without running it?

## Solution
Check out the reference in Hit: [strings](https://linux.die.net/man/1/strings)
``` shell
$wget https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
$strings -f strings
...
$strings -f strings | grep -e "picoCTF{\w*}"
strings: picoCTF{5tRIng5_1T_827aee91}
```
``` plain
picoCTF{5tRIng5_1T_827aee91}
```

### Improving

