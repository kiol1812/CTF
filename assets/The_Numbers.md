# The Numbers
- Difficulty: Easy
- Category: `Cryptography`  
- Date: 2024-09-18  
tags: `picoCTF 2019`  
refer to [Source](https://play.picoctf.org/practice/challenge/68?page=5)

## Description
The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?

## Solution
``` shell
$wget https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png
$binwalk the_numbers.png
...
$exiftool the_numbers.png
...
$feh the_numbers.png # open the image.
```
Open the image, and will see that It have some numbers.
``` plain
16 9 3 15 3 20 6 { 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14 }
```
write a sample python script.
``` python
s = input()
slt = s.split(' ')
for a in slt:
    if a=='{':
        print('{', end='')
    elif a=='}':
        print('}', end='')
    else:
        print(chr(int(a)+64), end='')
```
``` shell
$echo "16 9 3 15 3 20 6 { 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14 }" | python de.py
PICOCTF{THENUMBERSMASON}
```
``` plain
PICOCTF{THENUMBERSMASON}
```

### Improving
