# Wave a flag
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-14  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/170?page=4)

## Description
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...

## Solution
``` shell
$wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
$chmod +x warm
$./warm
Hello user! Pass me a -h to learn what I can do!
$./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
```
``` plain
picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
```

### Improving
