# Forbidden Paths

---
## Objectivo
Can you get the flag?Here's the [website](http://saturn.picoctf.net:55827/).We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?


---
## Solución
``` bash


picoCTF{7h3_p47h_70_5ucc355_e5a6fcbc}

```
### `picoCTF{7h3_p47h_70_5ucc355_e5a6fcbc}`

---
## Notas adicionales

Se pude realizar un carga util al conocer la ruta en la que se ubica el archivo
../../../../../flag.txt

---
## Referencias
https://sag0li.com/picoctf-forbidden-paths-writeup