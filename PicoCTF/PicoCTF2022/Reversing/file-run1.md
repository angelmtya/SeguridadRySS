# file-run1

---
## Objectivo

A program has been provided to you, what happens if you try to run it on the command line?Download the program [here](https://artifacts.picoctf.net/c/309/run).

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ wget https://artifacts.picoctf.net/c/310/run
--2022-11-28 17:11:31--  https://artifacts.picoctf.net/c/310/run
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.17, 13.249.74.22, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.17|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16736 (16K) [application/octet-stream]
Saving to: ‘run’

run                               100%[============================================================>]  16.34K  --.-KB/s    in 0.005s  

2022-11-28 17:11:32 (3.51 MB/s) - ‘run’ saved [16736/16736]

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls
run
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ chmod 777 run 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ./run 
The flag is: picoCTF{U51N6_Y0Ur_F1r57_F113_47cf2b7b}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 




```

---
## Notas adicionales


---
## Referencias

	