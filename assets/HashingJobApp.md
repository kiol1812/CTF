# HashingJobApp
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-14  
tags: `Beginner picoMini 2022` `hashing` `nc` `shell` `Python`  
refer to [Source]()

## Solution
Use online tool to produce md5 string.
``` shell
$nc saturn.picoctf.net 64218
Please md5 hash the text between quotes, excluding the quotes: 'amputations'
Answer:
1A132BA924B6EF44599DBDBF99CA6CD1
1A132BA924B6EF44599DBDBF99CA6CD1
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Japan'
Answer:
53A577BB3BC587B0C28AB808390F1C9B
53A577BB3BC587B0C28AB808390F1C9B
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'homeless shelters'
Answer:
ED96F5BCF2CB76F423A92190358B6881
ED96F5BCF2CB76F423A92190358B6881
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_3eb82b73}
```
``` plain
picoCTF{4ppl1c4710n_r3c31v3d_3eb82b73}
```

### Improving
