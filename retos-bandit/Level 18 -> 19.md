# Level 18 -> 19
---
## Objectivo
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

---
## Datos de acceso
- user -> **bandit18**
- Passwor -> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución
``` shell
angel@angelMnt:~$ ssh  bandit18@bandit.labs.overthewire.org -p 2220 ls
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password: 
readme
angel@angelMnt:~$ ssh  bandit18@bandit.labs.overthewire.org -p 2220 cat readme
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password: 
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
angel@angelMnt:~$ 

``` 
---
## Notas adicionales
Madar una cat junto con la conexión, que se ejecuta antes de que se cierre la sesión.

---
## Referencias
