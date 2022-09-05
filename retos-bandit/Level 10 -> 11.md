# Level 10 -> 11
---
## Objectivo

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data.

---
## Datos de acceso
- user -> **bandit10**
- Password -> G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
- host ->  **bandit.labs.overthewire.org**

---
## Solución
``` shell
bandit10@bandit:~$ cat data.txt | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
bandit10@bandit:~$ 
``` 
---
## Notas adicionales
#### Comandos linux

**base64** 
Permite codificar o descodificar en base64.
**-d**
Indica que se va a decodificar.
**-e**
Indica que se va a codificar.

---
## Referencias
https://linuxhint.com/bash_base64_encode_decode/

https://en.wikipedia.org/wiki/Base64

