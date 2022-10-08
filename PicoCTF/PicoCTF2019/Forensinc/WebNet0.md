# WebNet0


---
## Objectivo

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2019/forensics/WebNet0$ ssldump -r capture.pcap -k picopico.key -d | grep picoCTF{ -A 2 -B 2
    0a 43 6f 6e 74 65 6e 74 2d 45 6e 63 6f 64 69 6e    .Content-Encodin
    67 3a 20 67 7a 69 70 0d 0a 50 69 63 6f 2d 46 6c    g: gzip..Pico-Fl
    61 67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67    ag: picoCTF{nong
    73 68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63    shim.shrimp.crac
    6b 65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c    kers}..Content-L
--
    43 6f 6e 74 65 6e 74 2d 45 6e 63 6f 64 69 6e 67    Content-Encoding
    3a 20 67 7a 69 70 0d 0a 50 69 63 6f 2d 46 6c 61    : gzip..Pico-Fla
    67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67 73    g: picoCTF{nongs
    68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63 6b    him.shrimp.crack
    65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c 65    ers}..Content-Le
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2019/forensics/WebNet0$ 
picoCTF{nongshim.shrimp.crackers}
```
### `picoCTF{nongshim.shrimp.crackers}
---
**SSL** es el acrónimo de Secure Sockets Layer , la tecnología estándar para mantener segura una conexión a Internet, así como para proteger cualquier información confidencial que se envía entre dos sistemas e impedir que los delincuentes lean y modifiquen cualquier dato que se transfiera.

El protocolo TLS  es solo una versión actualizada y más segura de SSL.

## Notas adicionales
### Comandos linux
**ssldump**
_ssldump_ es un analizador de protocolos de red SSL/TLS. Identifica las conexiones TCP en la interfaz de red elegida e intenta interpretarlas como tráfico SSL/TLS. Cuando identifica el tráfico SSL/TLS, decodifica los registros y los muestra en forma de texto en la salida estándar. Si se le proporciona el material de clave adecuado, también descifrará las conexiones y mostrará el tráfico de datos de la aplicación.
-r paquetes.
-k Llaves.
-d decodificar.

**grep**
**-A** lineas anteriores.
**-B** lineas posteriores.


---
## Referencias
https://www.websecurity.digicert.com/es/es/security-topics/what-is-ssl-tls-https

https://linux.die.net/man/1/ssldump


	