# WebDecode
- Difficulty: Easy
- Category: `Web Exploitation`  
- Date: 2024-09-11   
tags: `picoCTF 2024` `browser_webshell_solvable`  
refer to [Source](https://play.picoctf.org/practice/challenge/427)

## Solution
press `f12` to view element. then can find this.
``` html
<section class="about" notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMTBmOTM3NmZ9">
   <h1>
    Try inspecting the page!! You might find it there
   </h1>
   <!-- .about-container -->
</section>
```
use online tool to decode. In this case, it's base64.
``` plain
picoCTF{web_succ3ssfully_d3c0ded_10f9376f}
```

### Improving


