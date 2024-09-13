# First find
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-13  
tags: `picoGym Exclusive`  
refer to [Source](https://play.picoctf.org/practice/challenge/320?page=2)

## Solution
Unzip this archive and find the file named 'uber-secret.txt'.
``` shell
$wget https://artifacts.picoctf.net/c/501/files.zip
$unzip files.zip
$find ./files -name "uber-secret.txt"
./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
$cat ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}
```
``` plain
picoCTF{f1nd_15_f457_ab443fd1}
```

### Improving
