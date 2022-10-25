# Packets Primer
---
## Objectivo

Download the packet capture file and use packet analysis software to find the flag.

-   [Download packet capture](https://artifacts.picoctf.net/c/200/network-dump.flag.pcap)

---
## Solución

``` sh

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ ssldump -r network-dump.flag.pcap -d
New TCP connection #1: 10.0.2.15(48750) <-> 10.0.2.4(9000)
0.0012 (0.0012)  C>S
---------------------------------------------------------------
p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ 0 1 b 0 a 0 d 6 }
---------------------------------------------------------------

Cleaning 1 remaining connection(s) from connection pool
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ ssldump -r network-dump.flag.pcap -d | grep { | tr -d ' '
picoCTF{p4ck37_5h4rk_01b0a0d6}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ 


```

---
## Notas adicionales

### Comandos linux


---
## Referencias
