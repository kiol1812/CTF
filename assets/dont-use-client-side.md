# dont-use-client-side
- Difficulty: Easy
- Category: `Web Exploitation`  
- Date: 2024-09-18  
tags: `picoCTF 2019`  
refer to [Source](https://play.picoctf.org/practice/challenge/66?page=5)

## Description
Can you break into this super secure portal? https://jupiter.challenges.picoctf.org/problem/37821/ ([link](https://jupiter.challenges.picoctf.org/problem/37821/)) or http://jupiter.challenges.picoctf.org:37821

## Solution
press `f12` and check the source.
can find out it loaded verify function.
``` javascript
<script type="text/javascript">
  function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == 'a3c8') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_1') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == '9}') {
                  alert("Password Verified")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
    
  }
</script>
```
``` plain
picoCTF{no_clients_plz_1a3c89}
```

### Improving

