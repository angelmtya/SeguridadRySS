# Glitch Cat

---
## Objectivo
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 51109`


---
## Solución
``` bash
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nc saturn.picoctf.net 51109
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
^C
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3
Python 3.8.10 (default, Jun 22 2022, 20:18:18) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x62)
'b'
>>> chr(0x64)
'd'
>>> chr(0x61)
'a'
>>> chr(0x36)
'6'
>>> chr(0x38)
'8'
>>> chr(0x66)
'f'
>>> chr(0x37)
'7'
>>> chr(0x35
... )
'5'
>>> exit()
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 
picoCTF{gl17ch_m3_n07_bda68f75}

```
### `picoCTF{gl17ch_m3_n07_bda68f75}`

---
## Notas adicionales

---
## Referencias
