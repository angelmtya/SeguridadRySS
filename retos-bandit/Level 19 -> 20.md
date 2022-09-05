
# Level 19 -> 20
---
## Objectivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

---
## Datos de acceso
- user -> **bandit19**
- Passwor ->awhqfNnAbc1naukrpqDYcF95h7HoMTrC
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución
``` shell
bandit19@bandit:~$ file bandit20-do 
bandit20-do: setuid ELF 32-bit LSB executable, Intel 80386, version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux.so.2, BuildID[sha1]=532dd885fc767d9543f333a2803588ea6fe2a83f, for GNU/Linux 3.2.0, not stripped
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit19@bandit:~$ 
``` 
---
## Notas adicionales

**Setuid y setgid**
Permiten a los usuarios ejecutar un ejecutable con los permisos del sistema de archivos del propietario o grupo del ejecutable respectivamente y cambiar el comportamiento en los directorios.

---
## Referencias
https://en.wikipedia.org/wiki/Setuid