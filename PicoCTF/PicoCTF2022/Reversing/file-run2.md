# file-run2

---
## Objectivo

Another program, but this time, it seems to want some input. What happens if you try to run it on the command line with input "Hello!"?Download the program [here](https://artifacts.picoctf.net/c/352/run).

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ wget https://artifacts.picoctf.net/c/353/run
--2022-11-28 17:12:48--  https://artifacts.picoctf.net/c/353/run
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.192.2, 99.84.192.11, 99.84.192.79, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.192.2|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16816 (16K) [application/octet-stream]
Saving to: ‘run’

run                               100%[============================================================>]  16.42K  --.-KB/s    in 0.007s  

2022-11-28 17:12:49 (2.14 MB/s) - ‘run’ saved [16816/16816]

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls -l
total 20
-rw-rw-r-- 1 angel angel 16816 mar 15  2022 run
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ chmod 777 run 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ./run 
Run this file with only one argument.
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ./run hola
Won't you say 'Hello!' to me first?
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ./run Hello
Won't you say 'Hello!' to me first?
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ./run Hello!
The flag is: picoCTF{F1r57_4rgum3n7_f65ed63e}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 


```

### `picoCTF{F1r57_4rgum3n7_f65ed63e}

---
## Notas adicionales


---
## Referencias

	