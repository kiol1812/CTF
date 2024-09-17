# fixme1.py
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-14  
tags: `Beginner picoMini 2022` `Python`  
refer to [Source](https://play.picoctf.org/practice/challenge/240?page=3)

## Solution
``` shell
$wget https://artifacts.picoctf.net/c/25/fixme1.py
$python fixme1.py
  File "/home/kiol1812/ctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
```
``` shell
$vim fixme1.py
$python fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```
``` plain
picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```

### Improving
