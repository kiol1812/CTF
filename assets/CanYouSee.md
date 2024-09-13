# CanYouSee
- Difficulty: Easy
- Category: `Forensics`  
- Date: 2024-09-12  
tags: `picoCTF 2024` `browser_webshell_solvable`  
refer to [Source](https://play.picoctf.org/practice/challenge/408?page=2)

## Solution
``` shell
$wget https://artifacts.picoctf.net/c_titan/130/unknown.zip
$unzip unknown.zip
$ls
ukn_reality.jpg  unknown.zip
$exiftool ukn_reality.jpg
ExifTool Version Number         : 12.96
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:03:12 08:05:55+08:00
File Access Date/Time           : 2024:09:12 01:48:59+08:00
File Inode Change Date/Time     : 2024:09:12 01:49:24+08:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
$echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg==" | base64 -d
picoCTF{ME74D47A_HIDD3N_6a9f5ac4}
```
``` plain
picoCTF{ME74D47A_HIDD3N_6a9f5ac4}
```

### Improving
