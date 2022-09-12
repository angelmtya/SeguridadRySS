#  Obedient Cat

---
## Objectivo

This file has a flag in plain sight (aka "in-the-clear"). Download flag.

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ wget https://mercury.picoctf.net/static/0e428b2db9788d31189329bed089ce98/flag
--2022-09-11 23:54:18--  https://mercury.picoctf.net/static/0e428b2db9788d31189329bed089ce98/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: ‘flag’

flag                              100%[============================================================>]      34  --.-KB/s    in 0s      

2022-09-11 23:54:18 (2.83 MB/s) - ‘flag’ saved [34/34]

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat flag
picoCTF{s4n1ty_v3r1f13d_2fd6ed29}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 
```

### `picoCTF{s4n1ty_v3r1f13d_2fd6ed29}`

---
## Notas adicionales

### Comandos linux

**Wget**
 Puedes usarlo para recuperar contenido y archivos de varios servidores web. El nombre es una combinación de **World Wide Web** y la palabra **get**. Admite descargas a través de FTP, SFTP, HTTP y HTTPS.


---
## Referencias

https://www.hostinger.mx/tutoriales/usar-comando-wget/#%C2%BFQue_es_el_Comando_Wget
	