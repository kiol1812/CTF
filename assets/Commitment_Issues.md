# Commitment Issues
- Difficulty: Easy
- Category: `General Skills`  
- Date: 2024-09-12  
tags: `picoCTF 2024` `browser_webshell_solvable` `git`  
refer to [Source](https://play.picoctf.org/practice/challenge/411?page=2)

## Solution
``` shell
$git log --oneline
42942c9 (HEAD -> master) remove sensitive info
b562f0b create flag
$git diff 4294 b562     
diff --git a/message.txt b/message.txt
index d552d1e..0e0fefc 100644
--- a/message.txt
+++ b/message.txt
@@ -1 +1 @@
-TOP SECRET
+picoCTF{s@n1t1z3_c785c319}
```
``` plain
picoCTF{s@n1t1z3_c785c319}
```

### Improving
