# Static ain't always noise
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-15  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/163?page=4)

## Description
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!

## Solution
``` shell
$wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
$wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
$cat ltdis.sh
...
$chmod +x ltdis.sh
$./ltdis.sh static
$cat static.ltdis.strings.txt 
...
picoCTF{d15a5m_t34s3r_f5aeda17}
...
```
``` plain
picoCTF{d15a5m_t34s3r_f5aeda17}
```

### Improving
