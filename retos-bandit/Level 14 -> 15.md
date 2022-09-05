# Level 14 -> 15
---
## Objectivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

---
## Datos de acceso
- user -> **bandit14**
- Passwor -> fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución
``` shell
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$ nc localhost 30000 -v 
Connection to localhost (127.0.0.1) 30000 port [tcp/*] succeeded!
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
``` 
---
## Notas adicionales
Los puertos pueden configurarse para que realicen procesos.

#### Comandos linux
**nc** Mediante el comando puedes conectarte a los puertos TCP/UDP de un host.
**-l** Sirve para que Netcat abra un puerto y se mantenga ala escucha
**-v** Se usa para mostrar información acerca de la conexión.

---
## Referencias
https://www.neoguias.com/comando-nc/

https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html
