# logon
- Difficulty: Easy
- Category: `Web Exploitation`  
- Date: 2024-09-19  
tags: `picoCTF 2019`  
refer to [Source](https://play.picoctf.org/practice/challenge/46?page=5)

## Description
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? https://jupiter.challenges.picoctf.org/problem/13594/ ([link](https://jupiter.challenges.picoctf.org/problem/13594/)) or http://jupiter.challenges.picoctf.org:13594

## Solution
Open the website, and check out source. we'll find out that it has not show js verify function for us. So, next we check out what will happen when we login as Joe or other one. Finally, we find out it use post request and carry two value, name and password. And it can be change in cookie.
Change admin value from False to True. Then we will get the flag

``` plain
picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}
```

### Improving

