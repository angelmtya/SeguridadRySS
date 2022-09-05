# Level 8 -> 9
---
## Objectivo

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

---
## Datos de acceso
- user -> **bandit8**
- Password -> TESKZC0XvTetK0S9xNwm25STk5iWrBvP
- host ->  **bandit.labs.overthewire.org**

---
## Solución
``` shell
bandit8@bandit:~$ ls 
data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$ 
``` 
---
## Notas adicionales
#### Comandos linux

**sort**  Permite ordenar lineas de texto.

**uniq** Permite filtrar las lineas de texto.
**-u**     Muestra solo las lineas unicas
-C cuenta las el numero de ocurrencias.
-d muestra todas menos la que no se repite.

**|**    Envía información de un comando a otro

---
## Referencias
https://ryanstutorials.net/linuxtutorial/piping.php

https://www.ibidemgroup.com/edu/tutorial-sort-linux-unix/#:~:text=M%C3%A1s%20informaci%C3%B3n-,%C2%BFQu%C3%A9%20es%20el%20comando%20sort%3F,y%20tambi%C3%A9n%20puede%20eliminar%20duplicados.

https://www.geeksforgeeks.org/uniq-command-in-linux-with-examples/

