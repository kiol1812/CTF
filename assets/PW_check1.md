# PW Check 1
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-13  
tags: `Beginner picoMini 2022` `password_cracking`  
refer to [Source](https://play.picoctf.org/practice/challenge/245?page=3)

## Solution
``` shell
$wget https://artifacts.picoctf.net/c/12/level1.py
$wget https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
$cat level1.py
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level1.flag.txt.enc', 'rb').read()

def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "8713"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")

level_1_pw_check()
$python level1.py
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
```
``` plain
picoCTF{545h_r1ng1ng_1b2fd683}
```

### Improving
