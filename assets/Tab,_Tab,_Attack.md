# Tab, Tab, Attack
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-14  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/176?page=4)

## Description
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip)

## Solution
``` shell
$wget https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip
$unzip Addadshashanammu.zip
$ls
$cd Addadshashanammu
$grep -r pico ./*
grep: ./Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet: binary file matches
$cd ./Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku
$./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_6f332f10}
```
``` plain
picoCTF{l3v3l_up!_t4k3_4_r35t!_6f332f10}
```

### Improving
