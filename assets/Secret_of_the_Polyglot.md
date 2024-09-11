# Secret of the Polyglot
- Difficulty: Easy
- Category: `Forensics`  
- Date: 2024-09-11  
tags: `picoCTF 2024` `file)format` `polyglot`  
refer to [Source](https://play.picoctf.org/practice/challenge/423)

## Solution
``` shell
$wget https://artifacts.picoctf.net/c_titan/7/flag2of2-final.pdf
$cat flag
�PNG...
```
In windows, just open .pdf file. could seen this
``` plain
1n_pn9_&_pdf_53b741d6}
```
Change file type to .png(`f2` to rewrite .pdf to .png). could seen this.
``` plain
picoCTF{f1u3n7_
```
``` plain
picoCTF{f1u3n7_1n_pn9_&_pdf_53b741d6}
```

### Improving
Use command line interface to solve this problem.