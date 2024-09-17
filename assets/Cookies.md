# Cookies
- Difficulty: Easy
- Category: `Web Exploitation`  
- Date: 2024-09-14  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/173?page=4)

## Description
Who doesn't love cookies? Try to figure out the best one. http://mercury.picoctf.net:54219/

## Solution
In the website, press `f12` to check out `Application>Cookies`. Then can see it has a name:value that call name, and value is between -1 and 24(after try many times). After try many times, when it's 18, can get the flag. 
``` plain
picoCTF{3v3ry1_l0v3s_c00k135_96cdadfd}
```

### Improving
How to reduce times that check what cookies is.