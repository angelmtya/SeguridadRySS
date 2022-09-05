# Level 7 -> 8
---
## Objectivo

The password for the next level is stored in the file **data.txt** next to the word **millionth**

---
## Datos de acceso
- user -> **bandit7**
- Password ->z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
- host ->  **bandit.labs.overthewire.org**

---
## Solución
``` shell
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ grep millionth data.txt 
millionth	TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ 
``` 
---
## Notas adicionales
#### Comandos linux

**grep**
Permite buscar una palabra o patron, e imprimir las líneas que la contienen.

---
## Referencias
https://www.hostinger.mx/tutoriales/comando-grep-linux
