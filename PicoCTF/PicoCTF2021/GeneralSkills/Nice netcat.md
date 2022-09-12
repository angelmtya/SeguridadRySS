# Nice netcat...

---
## Objectivo

There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 49039`, but it doesn't speak English...

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nano convertidorASCIItoChar.py
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat convertidorASCIItoChar.py 
entrada = input().split()

for i in entrada:
	a = int(i)
	print(chr(a), end="")

print("")
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nc mercury.picoctf.net 21135 | tr '\n' ' ' >  nice_cat 
 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat nice_cat 
112  105  99  111  67  84  70  123  103  48  48  100  95  107  49  116  116  121  33  95  110  49  99  51  95  107  49  116  116  121  33  95  97  102  100  53  102  100  97  52  125  10  
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 convertidorASCIItoChar.py < nice_cat 
picoCTF{g00d_k1tty!_n1c3_k1tty!_afd5fda4}

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 
```
#### `picoCTF{g00d_k1tty!_n1c3_k1tty!_afd5fda4}`

---
## Notas adicionales

Programa que permite convertir ASCII a char
convertidorASCIItoChar.py

### Comandos linux

**tr**
Puede operar y transformar texto desde la entrada estándar hasta la salida estándar

tr '\n'  '  '  >  nice_cat 
comando que elimina los saltos de línea y guarda la salida en un archivo.


---
## Referencias

https://es.wikipedia.org/wiki/UTF-8

https://geekland.eu/uso-del-comando-tr-en-linux-y-unix-con-ejemplos/


	