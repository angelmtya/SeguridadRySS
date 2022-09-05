# Level 12 -> 13
---
## Objectivo

The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

---
## Datos de acceso
- user -> **bandit12**
- Password -> JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución
``` shell
bandit12@bandit:~$ mkdir /tmp/tmpmydir
bandit12@bandit:~$ cp data.txt /tmp/tmpmydir
bandit12@bandit:~$ cd  /tmp/tmpmydir
bandit12@bandit:/tmp/tmpmydir$ ls
data.txt
bandit12@bandit:/tmp/tmpmydir$ 
bandit12@bandit:/tmp/tmpmydir$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
bandit12@bandit:/tmp/tmpmydir$ 
``` 
---
## Notas adicionales

Una vez que el archivo esté en binario, se descomprime según el tipo de comprensión usando, el comando file ayuda a saber cómo está comprimido.

#### Comandos linux

**xxd**
Crea un volcado hexadecimal de un archivo. También puede convertir un volcado hexadecimal de nuevo a su forma binaria inicial.
**-r** Transforma de hexadecimal a binario.

**zcat** 
Es una utilidad de línea de comandos para ver el contenido de un archivo comprimido sin descomprimirlo, equivalente a gzip.

**bzcat** 
Permite comprimir archivos y directorios en memoria, equivalente a bzip2

**tar xO**
Permite comprimir archivos y directorios en memoria, equivalente a tar

---
## Referencias
https://es.linux-console.net/?p=2219

https://linux.die.net/man/1/bzcat

https://www.hostinger.mx/tutoriales/como-usar-comando-tar-linux
