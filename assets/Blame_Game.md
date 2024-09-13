# Blame Game
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-12  
tags: `picoCTF 2024` `browser_webshell_solvable` `git`  
refer to [Source](https://play.picoctf.org/practice/challenge/405?page=2)

## Solution
``` shell
$wget https://artifacts.picoctf.net/c_titan/156/challenge.zip
$unzip challenge.zip
$cd drop-in
$git log --oneline
... // could find out is too many commit to check
```
Use git blame \<filename> to check it has changed by which commit.
``` shell
$git blame message.py
0351e047 (picoCTF{@sk_th3_1nt3rn_d2d29f22} 2024-03-12 00:07:01 +0000 1) print("Hello, World!"
```
``` plain
picoCTF{@sk_th3_1nt3rn_d2d29f22}
```

### Improving
