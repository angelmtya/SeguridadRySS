# strings it


---
## Objectivo

Can you find the flag in file without running it?

---
## Solución

``` shell
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
--2022-09-11 20:53:17--  https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: ‘strings’

strings                           100%[============================================================>] 757.84K  1.26MB/s    in 0.6s    

2022-09-11 20:53:19 (1.26 MB/s) - ‘strings’ saved [776032/776032]

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls
bandit26.sshkey  strings
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ mv strings st
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls
bandit26.sshkey  st
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ strings st | grep pico
picoCTF{5tRIng5_1T_d66c7bb7}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 

```

### `picoCTF{5tRIng5_1T_d66c7bb7}`

---
## Notas adicionales
#### Comandos linux

**wget**
Esta es una herramienta libre que permite la descarga de contenidos desde servidores web de una forma simple y rápida.

**strings** 
Permite obtener los caracteres legibles de un archivo  binario no legible.
**grep**
Permite buscar una palabra o patron, e imprimir las líneas que la contienen.

---
## Referencias

https://www.ibm.com/docs/en/aix/7.2?topic=s-strings-command

https://linux.die.net/man/1/strings