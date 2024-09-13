# Endianness
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-12  
tags: `picoCTF 2024` `browser_webshell_solvable`  
refer to [Source](https://play.picoctf.org/practice/challenge/414?page=2)

## Solution
Look at Source code, and add line to print what little_endian and big_endian is.
Could find out that is each word's hex, and little_endian[0]=challenge_word[5].hex; little_endian[1]=challenge_word[4].hex; ...; big_endian[0]=challenge_word[0].hex; big_endian[1]=challenge_word[1].hex; ...;
``` shell
$nc titan.picoctf.net 55484
Welcome to the Endian CTF!
You need to find both the little endian and big endian representations of a word.
If you get both correct, you will receive the flag.
Word: kknbu
Enter the Little Endian representation: 75626e6b6b
Correct Little Endian representation!
Enter the Big Endian representation: 6b6b6e6275
Correct Big Endian representation!
Congratulations! You found both endian representations correctly!
Your Flag is: picoCTF{3ndi4n_sw4p_su33ess_cfe38ef0}
```
``` plain
picoCTF{3ndi4n_sw4p_su33ess_cfe38ef0}
```

### Improving
