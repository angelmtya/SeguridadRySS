# GDB Test Drive

---
## Objectivo
Can you get the flag?Download this [binary](https://artifacts.picoctf.net/c/116/gdbme).Here's the test drive instructions:

-   `$ chmod +x gdbme`
-   `$ gdb gdbme`
-   `(gdb) layout asm`
-   `(gdb) break *(main+99)`
-   `(gdb) run`
-   `(gdb) jump *(main+104)`

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2022/ReverseEngineering$ chmod +x gdbme
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2022/ReverseEngineering$ gdb gdbme
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
Reading symbols from gdbme...
(No debugging symbols found in gdbme)
(gdb) 
│   0x5555555553c1 <__libc_csu_init+49>     sar    $0x3,%rbp                                                                          │
│   0x5555555553c5 <__libc_csu_init+53>     je     0x5555555553e6 <__libc_csu_init+86>                                                │
│   0x5555555553c7 <__libc_csu_init+55>     xor    %ebx,%ebx                                                                          │
│   0x5555555553c9 <__libc_csu_init+57>     nopl   0x0(%rax)                                                                          │
│   0x5555555553d0 <__libc_csu_init+64>     mov    %r14,%rdx                                                                          │
│   0x5555555553d3 <__libc_csu_init+67>     mov    %r13,%rsi                                                                          │
│   0x5555555553d6 <__libc_csu_init+70>     mov    %r12d,%edi                                                                         │
│   0x5555555553d9 <__libc_csu_init+73>     callq  *(%r15,%rbx,8)                                                                     │
│   0x5555555553dd <__libc_csu_init+77>     add    $0x1,%rbx                                                                          │
│   0x5555555553e1 <__libc_csu_init+81>     cmp    %rbx,%rbp                                                                          │
│   0x5555555553e4 <__libc_csu_init+84>     jne    0x5555555553d0 <__libc_csu_init+64>                                                │
│   0x5555555553e6 <__libc_csu_init+86>     add    $0x8,%rsp                                                                          │
│   0x5555555553ea <__libc_csu_init+90>     pop    %rbx                                                                               │
│   0x5555555553eb <__libc_csu_init+91>     pop    %rbp                                                                               │
│   0x5555555553ec <__libc_csu_init+92>     pop    %r12                                                                               │
│   0x5555555553ee <__libc_csu_init+94>     pop    %r13                                                                               │
│   0x5555555553f0 <__libc_csu_init+96>     pop    %r14                                                                               │
│   0x5555555553f2 <__libc_csu_init+98>     pop    %r15                                                                               │
│   0x5555555553f4 <__libc_csu_init+100>    retq                                                                                      │
│   0x5555555553f5                              data16 nopw %cs:0x0(%rax,%rax,1)                                                      │
│   0x555555555400 <__libc_csu_fini>        endbr64                                                                                   │
│   0x555555555404 <__libc_csu_fini+4>      retq                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘
native No process In:                                                                                                     L??   PC: ?? 
(gdb) break *(main+99)
Breakpoint 1 at 0x132a
(gdb) run
Starting program: /home/angel/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2022/ReverseEngineering/gdbme

Breakpoint 1, 0x000055555555532a in main ()
(gdb) jump *(main+104)
Continuing at 0x55555555532f.
picoCTF{d3bugg3r_dr1v3_7776d758}

(gdb) terminate called after throwing an instance of 'gdb_exception_error'
                                                                          Aborted (core dumped)
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2022/ReverseEngineering$ 


```

### `picoCTF{d3bugg3r_dr1v3_7776d758}


---
## Notas adicionales
 GDB (Gnu Project Debugger) es una herramienta que permite entre otras cosas, correr el programa con la posibilidad de detenerlo cuando se cumple cierta condición, avanzar paso a paso, analizar que ha pasado cuando un programa se detiene o cambiar algunas cosas del programa como el valor de las variables.



---
## Referencias

https://lihuen.linti.unlp.edu.ar/index.php/C%C3%B3mo_usar_GDB