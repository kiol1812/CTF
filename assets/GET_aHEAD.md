# GET aHEAD
- Difficulty: Easy
- Category: `Web Exploitation`  
- Date: 2024-09-17  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/132?page=4)

## Description
Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:45028/

## Solution
Use `Brup Suite` to help solve this problem. First look at what is button do in this website. Then we can find out that it'll send GET or POST method. So we can open Brup Suite, and change method to HEAD to see what will happen.
``` response
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_775f2530}
Content-type: text/html; charset=UTF-8
```

``` plain
picoCTF{r3j3ct_th3_du4l1ty_775f2530}
```

### Improving
Use curl and change method with HEAD.