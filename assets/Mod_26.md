# Mod 26
- Difficulty: Easy
- Category: `Cryptography`  
- Date: 2024-09-17  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/144?page=4)

## Description
Cryptography can be easy, do you know what ROT13 is?  
`cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_jdJBFOXJ}`

## Solution
p->c, i->v : 16-3, 22-9
``` shell
$echo "cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_jdJBFOXJ}" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
picoCTF{next_time_I'll_try_2_rounds_of_rot13_wqWOSBKW}
```
``` plain
picoCTF{next_time_I'll_try_2_rounds_of_rot13_wqWOSBKW}
```

### Improving

