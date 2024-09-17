# information
- Difficulty: Easy
- Category: Easy  
- Date: 2024-09-14  
tags: `picoCTF 2021`  
refer to [Source](https://play.picoctf.org/practice/challenge/186?page=4)

## Description
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/d1375e383810d8d957c04eef9e345732/cat.jpg)

## Solution
``` shell
$wget https://mercury.picoctf.net/static/d1375e383810d8d957c04eef9e345732/cat.jpg
$binwalk cat.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             JPEG image data, JFIF standard 1.02
49661         0xC1FD          JBOOT STAG header, image id: 14, timestamp 0x37E26150, image size: 562276742 bytes, image JBOOT checksum: 0xC9A6, header JBOOT checksum: 0x40D4

$exiftool cat.jpg
perl: warning: Setting locale failed.
perl: warning: Please check that your locale settings:
        LANGUAGE = (unset),
        LC_ALL = (unset),
        LANG = "en_US.UTF-8"
    are supported and installed on your system.
perl: warning: Falling back to the standard locale ("C").
ExifTool Version Number         : 12.96
File Name                       : cat.jpg
Directory                       : .
File Size                       : 878 kB
File Modification Date/Time     : 2021:03:16 02:24:46+08:00
File Access Date/Time           : 2024:09:14 11:07:28+08:00
File Inode Change Date/Time     : 2024:09:14 11:07:17+08:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
$echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d
picoCTF{the_m3tadata_1s_modified}
```
``` plain
picoCTF{the_m3tadata_1s_modified}
```

### Improving
