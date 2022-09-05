# Level 6 -> 7
---
## Objectivo

The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size
---
## Datos de acceso
- user -> **bandit6**
- Password -> P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
- host ->  **bandit.labs.overthewire.org**

---
## Solución
``` shell
bandit6@bandit:/$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:/$ cat /var/lib/dpkg/info/bandit7.password 
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:/$ 
``` 
---
## Notas adicionales
#### Comandos linux

**find / -user bandit7 -group bandit6 -size 33c 2>/dev/null**
En el siguiente comando, se usa find para encontrar una archivo, de un usuario, grupo y tamaño específico, y los archivos o directorios que no se pudieron revisar, son redirigidos como errores.

**2>/dev/null**
2 indica los errores.

---
## Referencias
https://askubuntu.com/questions/350208/what-does-2-dev-null-mean#:~:text=Specifying%202%3E%2Fdev%2Fnull,printed%20out%20on%20the%20console.&text=%2Fdev%2Fnull%20is%20the%20standard,output%20that%20you%20want%20ignored.