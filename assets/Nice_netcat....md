# Nice netcat...
- Difficulty: Easy
- Category: `General Skills`  
- Date: 20224-09-17  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/156?page=4)

## Description
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 7449`, but it doesn't speak English...

## Solution
``` shell
$nc mercury.picoctf.net 7449
...
$touch tmp.txt
$nc mercury.picoctf.net 7449 >> tmp.txt
$touch print.py
$vim print.py
```
``` python
f = open("tmp.txt", 'r')
c=f.readline()
while(c):
    print(chr(int(c)), end='')
    c=f.readline()
```
``` shell
$python print.py
picoCTF{g00d_k1tty!_n1c3_k1tty!_f2d7cafa}
```
``` plain
picoCTF{g00d_k1tty!_n1c3_k1tty!_f2d7cafa}
```

### Improving
``` python
# improve.py
while True:
    try:
        n = int(input())
        print(chr(n), end='')
    except:
        print()
        break
```
``` shell
$nc mercury.picoctf.net 7449 | python improve.py
picoCTF{g00d_k1tty!_n1c3_k1tty!_f2d7cafa}
```