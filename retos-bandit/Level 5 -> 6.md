# Level 5 -> 6
---
## Objectivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

-   human-readable
-   1033 bytes in size
-   not executable

---
## Datos de acceso
- user -> **bandit5**
- Password ->lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
- host ->  **bandit.labs.overthewire.org**

---
## Solución
``` shell
bandit5@bandit:~/inhere$ find ./ -type f -size 1033c ! -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
``` 
---
## Notas adicionales
#### Comandos linux

**find**    Permite encontrar un archivo o directorio, con los parámetros dados.

**find ./ -type f -size 1033c ! -executable** 
El comando indica que se busca un archivo, que tiene un tamaño de 1033 caracteres y que no es ejecutable.

**!** Negar la función de un comando.

---
## Referencias
https://www.hostinger.mx/tutoriales/como-usar-comando-find-locate-en-linux/#:~:text=Utilizar%20el%20comando%20find%20en%20Linux%20para%20buscar%20archivos%20por,r%C3%A1pidas%20en%20todo%20el%20sistema.