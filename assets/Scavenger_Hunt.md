# Scavenger Hunt
- Difficulty: Easy
- Category: `Web Exploitation`  
- Date: 2024-09-15  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/161?page=4)

## Description
There is some interesting information hidden around this site http://mercury.picoctf.net:5080/. Can you find it?

## Solution
press `f12` to see html, css, javascript. Then will see part 1, 2 in css and html. and hava "How can I keep Google from indexing my website?" in script.js. Then search with that message. It will show some information about robots.txt.
``` plain
// http://mercury.picoctf.net:5080/robots.txt
User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?
```
`apache sever` `Access` -> .htaccess
``` plain
// http://mercury.picoctf.net:5080/.htaccess
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
```
`Mac` `Store` -> [DS_Store](https://buildthis.com/ds_store-files-and-why-you-should-know-about-them/)
``` plain
// http://mercury.picoctf.net:5080/.DS_Store
Congrats! You completed the scavenger hunt. Part 5: _35844447}
```

``` plain
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_35844447}
```

### Improving
