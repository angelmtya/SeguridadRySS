# Static ain't always noise

---
## Objectivo

Can you look at the data in this binary: static? This BASH script might help!

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls
convertidorASCIItoChar.py  flag  ltdis.sh  nice_cat  static  tr  warm
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ chmod 777 ltdis.sh 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ./ltdis.sh 
Attempting disassembly of  ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ./ltdis.sh static 
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat static.ltdis.strings.txt | grep pico
   1020 picoCTF{d15a5m_t34s3r_6f8c8200}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 
```

### `picoCTF{d15a5m_t34s3r_6f8c8200}`

Otra solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021$ strings -a -t x  static | grep picoCTF{
   1020 picoCTF{d15a5m_t34s3r_ae0b3ef2}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021$ 

```

---
## Notas adicionales

### Comandos linux

**Objdump**
Se usa para proporcionar información detallada sobre los archivos de objetos.




---
## Referencias
https://www.howtogeek.com/427805/how-to-use-the-strings-command-on-linux/

https://www.thegeekstuff.com/2012/09/objdump-examples/