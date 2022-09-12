# fixme1.py

---
## Objectivo

Fix the syntax error in this Python script to print the flag.

---
## Solución
``` bash
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 
convertme.py  fixme1.py     
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 fixme1.py 
  File "fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
    ^
IndentationError: unexpected indent
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nano fixme1.py 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 


```
### `picoCTF{1nd3nt1ty_cr1515_182342f7}`

---
## Notas adicionales
Error de identación

---
## Referencias
