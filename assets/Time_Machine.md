# Time Machine
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-11  
tags: `picoCTF 2024` `browser_webshell_solvable` `git`  
refer to [Source](https://play.picoctf.org/practice/challenge/425)

## Solution
``` shell
$wget https://artifacts.picoctf.net/c_titan/163/challenge.zip
$unzip changenge.zip
$ls
challenge.zip  drop-in
$cd drop-in
$ls -a
.git  message.txt
```
try, but failed.
``` shell
$git log --oneline
```
try
``` shell
$cat .git/logs/HEAD
0000000000000000000000000000000000000000 e65fedb3a72a16c577f4b17023b63997134b307d picoCTF <ops@picoctf.com> 1710202049 +0000     commit (initial): picoCTF{t1m3m@ch1n3_88c35e3b}
```
``` plain
picoCTF{t1m3m@ch1n3_88c35e3b}
```

### Improving
