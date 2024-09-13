# PW Check 2
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-13  
tags: `Beginner picoMini 2022` `password_cracking`  
refer to [Source](https://play.picoctf.org/practice/challenge/246?page=3)

## Solution
``` shell
$wget https://artifacts.picoctf.net/c/14/level2.py
$wget https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
$cat level2.py
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

flag_enc = open('level2.flag.txt.enc', 'rb').read()

def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")

level_2_pw_check()
```
Edit level2.py file:
```python
# user_pw = input("Please enter correct password for flag: ")
user_pw = chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)
```
Then
``` shell
$python level2.py
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
```
``` plain
picoCTF{tr45h_51ng1ng_9701e681}
```

### Improving
