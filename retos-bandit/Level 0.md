## Bandit Level-0
---
## Objetivo
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.

---
## Datos de acceso
- user -> **bandit0**
- Password -> **bandit0**
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución
``` shell
angel@angelMnt:~$ ssh bandit0@bandit.labs.overthewire.org -p 2220
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password: 
bandit0@bandit:~$ 
``` 

---
## Notas adicionales
**ssh**  
El protocolo Secure Shell ( SSH ) es un protocolo de red criptográfico para operar servicios de red de forma segura en una red no segura.se basan en una arquitectura cliente-servidor , conectando una instancia de cliente SSH con un servidor SSH 
**shh -p** 
Especificar el puerto a conectar.

---
## Referencias
https://www.wikihow.com/Use-SSH