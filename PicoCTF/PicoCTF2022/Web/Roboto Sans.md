# Roboto Sans

---
## Objectivo
The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:64710/) out.

---
## Solución
``` bash
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ curl http://saturn.picoctf.net:64710/robots.txt
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ curl http://saturn.picoctf.net:64710/js/myfile.txt
picoCTF{Who_D03sN7_L1k5_90B0T5_032f1c2b}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 


```

---
## Notas adicionales
Se decodifica base64
ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA== 

**robots.txt** 
El archivo robots.txt es un archivo de configuración que puede agregar al directorio raíz de su sitio de Web. Permite que un sitio web proporcione instrucciones para los robots de los motores de búsqueda, está disponible públicamente. Cualquiera puede acceder directamente para ver si hay páginas ocultas que no son indexadas.


---
## Referencias
https://gchq.github.io/CyberChef/#recipe=To_Base64('A-Za-z0-9%2B/%3D')From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YW5NdmJYbG1hV3hsTG5SNGRBPT0