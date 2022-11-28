# Need For Speed
---
## Objectivo
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/f9abc386dfb1309e687344783f208b20/need-for-speed).

---
## Solución
```sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2019/Reversing$ gdb need-for-speed
GNU gdb (Ubuntu 9.2-0ubuntu1~20.04.1) 9.2
Copyright (C) 2020 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<http://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from need-for-speed...
(No debugging symbols found in need-for-speed)
(gdb) call (int) header
$1 = 2264
(gdb) call (int) get_key
$2 = 2173
(gdb) run
Starting program: /home/angel/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2019/Reversing/need-for-speed 
Keep this thing over 50 mph!
============================

Creating key...
Not fast enough. BOOM!
[Inferior 1 (process 272917) exited normally]
(gdb) call (int) get_key
$3 = 1431652477
(gdb) set disa
disable-randomization  disassemble-next-line  disassembler-options   disassembly-flavor     
(gdb) set disassembly-flavor intel
(gdb) call (int) get_key
$4 = 1431652477
(gdb) call (int) get_key()
You can't do that without a process to debug.
(gdb) call (int) get_key()
You can't do that without a process to debug.
(gdb) call header()
You can''t do that without a process to debug.
(gdb) disassemble main
Dump of assembler code for function main:
   0x000055555555491a <+0>:	push   rbp
   0x000055555555491b <+1>:	mov    rbp,rsp
   0x000055555555491e <+4>:	sub    rsp,0x10
   0x0000555555554922 <+8>:	mov    DWORD PTR [rbp-0x4],edi
   0x0000555555554925 <+11>:	mov    QWORD PTR [rbp-0x10],rsi
   0x0000555555554929 <+15>:	mov    eax,0x0
   0x000055555555492e <+20>:	call   0x5555555548d8 <header>
   0x0000555555554933 <+25>:	mov    eax,0x0
   0x0000555555554938 <+30>:	call   0x55555555482f <set_timer>
   0x000055555555493d <+35>:	mov    eax,0x0
   0x0000555555554942 <+40>:	call   0x55555555487d <get_key>
   0x0000555555554947 <+45>:	mov    eax,0x0
   0x000055555555494c <+50>:	call   0x5555555548ac <print_flag>
   0x0000555555554951 <+55>:	mov    eax,0x0
   0x0000555555554956 <+60>:	leave  
   0x0000555555554957 <+61>:	ret    
End of assembler dump.

(gdb) run
Starting program: /home/angel/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2019/Reversing/need-for-speed 
Keep this thing over 50 mph!
============================

Creating key...
Not fast enough. BOOM!
[Inferior 1 (process 273095) exited normally]
(gdb) break main
Breakpoint 1 at 0x55555555491e
(gdb) run
Starting program: /home/angel/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2019/Reversing/need-for-speed 

Breakpoint 1, 0x000055555555491e in main ()
(gdb) call (int) header()
Keep this thing over 50 mph!
============================

$5 = 2
(gdb) call (int) get_key()
Creating key...
Finished
$6 = 9
(gdb) call (int) print_flag()
Printing flag:
PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}

$7 = 56
(gdb) 

```

### `PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}


---
## Notas adicionales
### Comandos linux

gdb
Es un depurador portable que se puede utilizar en varias plataformas Unix y funciona para varios lenguajes de programación como C, C++ y Fortran. GDB fue escrito por Richard Stallman en 1986. GDB es software libre distribuido bajo la licencia GPL.

GDB ofrece la posibilidad de trazar y modificar la ejecución de un programa. El usuario puede controlar y alterar los valores de las variables internas del programa.

(gdb) info functions 
-Información de las funciones

(gdb) disassemble función
-contenido de la función especificada

(gdb) break función
-establcer puntos de interupción

(gdb) call función
-Llamar funciones

---
## Referencias

https://es.wikipedia.org/wiki/GNU_Debugger
