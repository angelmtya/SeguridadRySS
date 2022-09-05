# Level 11 -> 12
---
## Objectivo

The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

---
## Datos de acceso
- user -> **bandit11**
- Password -> 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
- host ->  **bandit.labs.overthewire.org**

---
## Solución
``` shell
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$ 
``` 
---
## Notas adicionales

ROT13 es un cifrado de sustitución de letra simple que reemplaza una letra con la letra 13 después de ella en el alfabeto. 

#### Comandos linux
**tr**  Permite modificar cadenas, sustituir carácter y aplicar cifrados.

---
## Referencias
https://en.wikipedia.org/wiki/ROT13

https://stackoverflow.com/questions/5442436/using-rot13-and-tr-command-for-having-an-encrypted-email-address

https://conpilar.es/comando-tr-en-linux-con-ejemplos/

