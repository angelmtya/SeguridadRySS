# Level 9 -> 10
---
## Objectivo

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

---
## Datos de acceso
- user -> **bandit9**
- Password -> EN632PlfYiZbn3PhVK3XOGSlNInNE00t
- host ->  **bandit.labs.overthewire.org**

---
## Solución
``` shell
bandit9@bandit:~$ cat data.txt |  strings | grep ===
========== the*2i"4
========== password
Z)========== is
&========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$ 
``` 
---
## Notas adicionales
#### Comandos linux

**strings** 
Permite obtener los caracteres legibles de un archivo, de un archivo binario no legible.

---
## Referencias
howtogeek.com/427805/how-to-use-the-strings-command-on-linux/

