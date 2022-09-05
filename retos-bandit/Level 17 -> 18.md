# Level 17 -> 18
---
## Objectivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

---
## Datos de acceso
- user -> **bandit17**
- Passwor -> VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución
``` shell
bandit17@bandit:~$ diff passwords.old passwords.new 
42c42
< 09wUIyMU4YhOzl1Lzxoz0voIBzZ2TUAf
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
bandit17@bandit:~$
``` 
---
## Notas adicionales

#### Comandos linux
**diff** Compara las diferencias entre ficheros línea a línea.

---
## Referencias
https://eltallerdelbit.com/comando-diff-ejemplos/#:~:text=El%20comando%20diff%20compara%20las,entre%20archivos%20archivos%20de%20configuraci%C3%B3n.