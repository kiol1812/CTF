# First Grep
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-18  
tags: `picoCTF 2019`  
refer to [Source](https://play.picoctf.org/practice/challenge/85?page=5)

## Description
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file)? This would be really tedious to look through manually, something tells me there is a better way.

## Solution
``` shell
$Wget https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
$cat file
...
$grep -e "picoCTF{[A-Za-z0-9_]*}" file
picoCTF{grep_is_good_to_find_things_dba08a45}
```
``` plain
picoCTF{grep_is_good_to_find_things_dba08a45}
```

### Improving
``` plain
// regex
\w == [A-Za-z0-9_]
```
