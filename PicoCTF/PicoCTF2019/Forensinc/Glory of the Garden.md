# Glory of the Garden


---
## Objectivo

This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ xxd garden.jpg
00230550: a2bb bdac 9687 98e4 d3b2 e87f ffd9 4865  ..............He
00230560: 7265 2069 7320 6120 666c 6167 2022 7069  re is a flag "pi
00230570: 636f 4354 467b 6d6f 7265 5f74 6861 6e5f  coCTF{more_than_
00230580: 6d33 3374 735f 7468 655f 3379 3365 4264  m33ts_the_3y3eBd
00230590: 4264 3263 637d 220a                      Bd2cc}".
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 


```

### `picoCTF{more_than_m33ts_the_3y3eBdBd2cc}

---
## Notas adicionales

**Editor hexadecimal**
es un tipo de programa informático que permite a un usuario modificar archivos binarios. Los editores hexadecimales fueron diseñados para editar sectores de datos de disquetes o discos duros por lo que a veces se llaman "editores de sectores".


### Comandos linux

**xxd**
Editor que te permite realizar manipulaciones hexadímicas y binarias. Se usa comúnmente para hacer un volcado hexadecimal de un archivo dado o entrada estándar. También puede convertir un volcado hexadecimal a su forma binaria original.


---
## Referencias

https://es.wikipedia.org/wiki/Editor_hexadecimal

https://esgeeks.com/mejores-editores-hexadecimales-linux/

	