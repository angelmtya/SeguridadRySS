# Level 13 -> 14
---
## Objectivo

The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on

---
## Datos de acceso
- user -> **bandit13**
- Password -> wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución
``` shell
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost 
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$ 
'Descargar llave y aplicarlo local mente'
angel@angelMnt:~/Documentos/ClasesUAZ$ ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

``` 
---
## Notas adicionales

 **localhost** 
 is a hostname that refers to the machine you are working on

 **Clave SSH** 
 consiste en la generación de un par de claves que proporcionan dos largas cadenas de caracteres —una pública y una privada—. La clave públicase instala en cualquier servidor y luego se desbloquea mediante la conexión con un cliente SSH que hace uso de la **clave privada**. Si las dos claves coinciden, el servidor SSH permite el acceso sin necesidad de utilizar una contraseña.

---
## Referencias
https://www.stackscale.com/es/blog/configurar-llaves-ssh-servidor-linux/

https://help.ubuntu.com/community/SSH/OpenSSH/Keys
