# Level 1 -> 2

## Objectivo
The password for the next level is stored in a file called **-** located in the home directory.

---
## Datos de acceso
- user -> **bandit1**
- Password -> boJ9jbbUNNfktd78OOpsqOltutMc3MY1
- host ->  **bandit.labs.overthewire.org**
---
## Solución
``` shell
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ cat < -
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ 

``` 
---
## Notas adicionales
#### Comandos linux
**cat ./-**   Para imprimir archivos nombrados - , se puede especificar la ruta.
**cat  < -** También redireccionar la salida.
**cat  ruta**  Otra forma de imprimir es utilizando la ruta completa del archivo.

---
## Referencias
https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal