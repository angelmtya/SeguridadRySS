# Level 20 -> 21
---
## Objectivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think

---
## Datos de acceso
- user -> **bandit20**
- Passwor -> VxCazJaVykI6W36BkBU0mJTCM8rR95XT
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución

Terminal 1
``` shell
bandit20@bandit:~$ nc -lvp 2220
Listening on 0.0.0.0 2000
Connection received on localhost 59612
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
bandit20@bandit:~$ 

``` 

Terminal 2
``` shell
bandit20@bandit:~$ ./suconnect 2000
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
bandit20@bandit:~$ 
``` 

---
## Notas adicionales

#### Comandos linux

**nc**
Puedes conectarte a los puertos **TCP/UDP** de un host.
**-l** Sirve para que Netcat abra un puerto y se mantenga ala escucha. Se aceptará una única conexión de un único cliente antes de cerrarse.
**-p** Esta opción permite especificar el puerto al que conectarse.
**-v** Se usa para mostrar información acerca de la conexión.

---
## Referencias
https://www.neoguias.com/comando-nc/#Que_es_el_comando_nc

