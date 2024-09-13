# Interencodec
- Difficulty: Easy
- Category: `Cryptography`  
- Date: 2024-09-11  
tags: `picoCTF 2024` `base64` `browser_webshell_solvable` `caesar`  
refer to [Source](https://play.picoctf.org/practice/challenge/418)

## Solution
There with `base64` and `caesar` in tags.
So, first, use base64 to decode given file.
``` shell
$cat enc_flag
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyMHdNakV5TnpVNGZRPT0nCg==
$base64 -d enc_flag
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX20wMjEyNzU4fQ=='
```
Could seen this string still look like has been code with base64. So, do it again with cut command.
``` shell
$cut --help
...
  -d, --delimiter=DELIM   use DELIM instead of TAB for field delimiter
  -f, --fields=LIST       select only these fields;  also print any line
                            that contains no delimiter character, unless
                            the -s option is specified
...
```
``` shell
$base64 -d enc_flag | cut -d "'" -f2
d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX20wMjEyNzU4fQ==
$base64 -d enc_flag | cut -d "'" -f2 | base64 -d
wpjvJAM{jhlzhy_k3jy9wa3k_m0212758}
```
Then, use `caesar` to decode this string. write a sample python file to help decode.
``` python
str = input()
for c in str:
    if(c.isalpha()):
        if(c.islower() and ord(c)-ord('a')<7):
            print(chr(ord(c)-7+26), end='')
        elif(c.isupper() and ord(c)-ord('A')<7):
            print(chr(ord(c)-7+26), end='')
        else:
            print(chr(ord(c)-7), end='')
    else:
        print(c, end='')
```
``` plain
picoCTF{caesar_d3cr9pt3d_f0212758}
```

### Improving
