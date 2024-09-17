# Python Wrangling
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-14  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/166?page=4)

## Description
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/ende.py) using [this password](https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/pw.txt) to get [the flag](https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/flag.txt.en)?

## Solution
``` shell
$wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/ende.py
$wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/pw.txt
$wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/flag.txt.en
$cat ende.py
...
# pip install ...
$python ende.py -h
Usage: .\ende.py (-e/-d) [file]
Examples:
  To decrypt a file named 'pole.txt', do: '$ python .\ende.py -d pole.txt'
$cat pw.txt
192ee2db192ee2db192ee2db192ee2db
$python .\ende.py -d .\flag.txt.en
Please enter the password:192ee2db192ee2db192ee2db192ee2db
picoCTF{4p0110_1n_7h3_h0us3_192ee2db}
```
``` plain
picoCTF{4p0110_1n_7h3_h0us3_192ee2db}
```

### Improving
