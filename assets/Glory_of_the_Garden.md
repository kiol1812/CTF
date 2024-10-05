# Glory of the Garden
- Difficulty: Easy
- Category: `Forensics`  
- Date: 2024-09-19  
tags: `picoCTF 2019`  
refer to [Source](https://play.picoctf.org/practice/challenge/44?page=5)

## Description
This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.

## Solution
Hit say that "what is a hex editor"
``` shell
$wget https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg
$hexedit garden.jpg
...
# in editor
>> ctrl+r 70 69 63 6F 43 54 46 # picoCTF (hex)
```
Search hexa string in editor, then we will find out flag is in the end of file.
``` plain
picoCTF{more_than_m33ts_the_3y3657BaB2C}
```

### Improving
