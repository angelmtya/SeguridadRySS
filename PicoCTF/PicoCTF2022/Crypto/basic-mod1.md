
### basic-mod1

---
### Objectivo

We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/394/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

---
### Solución
``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat message.txt 
202 137 390 235 114 369 198 110 350 396 390 383 225 258 38 291 75 324 401 142 288 397 angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ^C
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nano mod1.py
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nano mod1.py
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 
junta_imagen.py  mod1.py          
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 mod1.py 
17 26 20 13 3 36 13 36 17 26 20 13 3 36 1 32 1 28 31 31 29 27 angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 
r  0  u   n d _  n  _  r   0  u  n  d _ b  6  b  2 5   5 3  1

```
picoCTF{R0UND_N_R0UND_B6B25531}
1 32 1 28 31 31 29 27 
B 6   B  2   5  5   3    1

0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 
a b c d  e f g h i  j    k   l    m  n   o  p   q   r   s   t   u   v    w   x   y   z

26 27 28 29 30 31 32 33 34 35 
0    1    2   3   4    5  6    7   8    9

---
### Notas adicionales


---
### Referencias

https://github.com/arvindshima/PicoCTF-2022/blob/main/Cryptography/basic-mod1.md
