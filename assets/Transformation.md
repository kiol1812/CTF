# Transformation
- Difficulty: Easy
- Category: `Reverse Engineering`  
- Date: 2024-09-17  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/104?page=4)

## Description
I wonder what this really is... [enc](https://mercury.picoctf.net/static/77a2b202236aa741e988581e78d277a6/enc) ''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])

## Solution
``` shell
$wget https://mercury.picoctf.net/static/77a2b202236aa741e988581e78d277a6/enc
$cat enc
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸強㕤㐸㤸扽
$touch code.py | vim code.py
```
``` python
flag="pico"
print(''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)]))
```
``` shell
$python code.py
灩捯
```
``` python
# code.py reverse original program
flag = "灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸強㕤㐸㤸扽"
#print(''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)]))
print(''.join([chr(ord(flag[i])>>8)+chr(ord(flag[i])&255) for i in range(0, len(flag))]))
```
``` shell
$python code.py
picoCTF{16_bits_inst34d_of_8_75d4898b}
```

``` plain
picoCTF{16_bits_inst34d_of_8_75d4898b}
```

### Improving
