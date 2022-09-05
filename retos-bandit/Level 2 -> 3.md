# Level 2 -> 3
---
## Objectivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory

---
## Datos de acceso
- user -> **bandit2**
- Password -> rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
- host ->  **bandit.labs.overthewire.org**

---
## Solución
``` shell
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename 
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ cat "spaces in this filename" 
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ 

``` 
---
## Notas adicionales
Un archivo que tiene el nombre con espacio puede ser seleccionado al encerrar el nombre entre comillas dobles o escribir el inicio del nombre y dar tabulador.


---
## Referencias
https://docs.microsoft.com/en-us/troubleshoot/windows-server/deployment/filenames-with-spaces-require-quotation-mark#:~:text=Spaces%20are%20allowed%20in%20long,word%20to%20specify%20a%20parameter.