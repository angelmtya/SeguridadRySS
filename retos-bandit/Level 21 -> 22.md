# Level 21 -> 22
---
## Objectivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

---
## Datos de acceso
- user -> **bandit21**
- Passwor -> WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución

``` shell
bandit21@bandit:~$ ls
bandit21@bandit:~$ cd /etc/cron.d
bandit21@bandit:/etc/cron.d$ ls
cronjob_bandit15_root  cronjob_bandit17_root  cronjob_bandit22  cronjob_bandit23  cronjob_bandit24  cronjob_bandit25_root
bandit21@bandit:/etc/cron.d$ cat cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit22.sh 
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:/etc/cron.d$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
bandit21@bandit:/etc/cron.d$

``` 



---
## Notas adicionales

#### Comandos linux

**cron y crontab**
Permiten realizar una determinada tarea (o varias) en un determinado tiempo.


---
## Referencias
https://www.redeszone.net/tutoriales/servidores/cron-crontab-linux-programar-tareas/
