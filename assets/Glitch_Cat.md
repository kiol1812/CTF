# Glitch Cat
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-14  
tags: `Beginner picoMini 2022` `nc` `shell` `Python`  
refer to [Source]()

## Solution
``` shell
$nc saturn.picoctf.net 54292
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
$python
Python 3.12.5 (main, Aug  9 2024, 08:20:41) [GCC 14.2.1 20240805] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}')
picoCTF{gl17ch_m3_n07_a4392d2e}
>>> exit()
```
``` plain
picoCTF{gl17ch_m3_n07_a4392d2e}
```

### Improving
