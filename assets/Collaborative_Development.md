# Collaborative Development
- Difficulty: Easy
- Category: `General Skills`  
- Date: 20224-09-12  
tags: `picoCTF 2024` `browser_webshell_solcable` `git`  
refer to [Source](https://play.picoctf.org/practice/challenge/410?page=2)

## Solution
There is Hint mention `git branch -a`.
``` shell
$git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
$git diff feature/part-1
diff --git a/flag.py b/flag.py
index 6e17fb3..77d6cec 100644
--- a/flag.py
+++ b/flag.py
@@ -1,2 +1 @@
 print("Printing the flag...")
-print("picoCTF{t3@mw0rk_", end='')
\ No newline at end of file
$git merge feature/part-1
$git merge feature/part-2
$git add . | git commit -m "fix conflict"
$git merge feature/part-3
$git add . | git commit -m "complete"
$python flag.py
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_798f9981}
```
``` plain
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_798f9981}
```

### Improving
