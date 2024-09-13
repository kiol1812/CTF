# Includes
- Difficulty: Easy
- Category: `Web Exploitation`  
- Date: 2024-09-13  
tags: `picoCTF 2022` `inspector`  
refer to [Source](https://play.picoctf.org/practice/challenge/274?page=3)

## Solution
press `f12` to inspect html. can see that button call a function from `script.js`, and it's store in `Sources`. check script can find a part of flag like:
``` javascript
//  f7w_2of2_df589022}
```
Then check style.css that also store in `Sources`.
``` css
/*  picoCTF{1nclu51v17y_1of2_  */
```
``` plain
picoCTF{1nclu51v17y_1of2_f7w_2of2_df589022}
```

### Improving
