# Level 4 -> 5
---
## Objectivo
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

---
## Datos de acceso
- user -> **bandit4**
- Password ->2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
- host ->  **bandit.labs.overthewire.org**

---
## Solución
``` shell
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$ 

``` 
---
## Notas adicionales
#### Comandos linux
**file**  Permite saber el formato y tipo de un archivo.

---
## Referencias
https://es.wikipedia.org/wiki/File_(Unix)#:~:text=El%20comando%20file%20es%20una,y%20formato%20de%20un%20archivo.&text=Sistema%20de%20archivos%3A%20se%20intenta,funci%C3%B3n%20(system%20call)%20stat.