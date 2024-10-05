# Bases
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-18  
tags: `picoCTF 2019`  
refer to [Source](https://play.picoctf.org/practice/challenge/67?page=5)

## Description
What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

## Solution
``` shell
$echo "bDNhcm5fdGgzX3IwcDM1" | base64 -d
l3arn_th3_r0p35
```
``` plain
picoCTF{l3arn_th3_r0p35}
```

### Improving
