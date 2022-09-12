# Wave a flag

---
## Objectivo

Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls
flag  warm
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls -l
total 16
-rw-rw-r-- 1 angel angel    34 mar 16  2021 flag
-rw-rw-r-- 1 angel angel 10936 mar 15  2021 warm
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ chmod 777 warm 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ./warm 
Hello user! Pass me a -h to learn what I can do!
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_f0668f62}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 


```

### `picoCTF{b1scu1ts_4nd_gr4vy_f0668f62}`

---
## Notas adicionales

---
## Referencias

