# Level 16 -> 17
---
## Objectivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

---
## Datos de acceso
- user -> **bandit16**
- Passwor -> JQttfApK4SeyHwDlI9SXGR50qclOAil1
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución
``` shell
bandit16@bandit:~$ nmap -p 31000-32000  localhost 

Starting Nmap 7.40 ( https://nmap.org ) at 2022-02-25 00:37 CET
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00035s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.08 seconds

bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
depth=0 CN = localhost
verify error:num=18:self signed certificate
verify return:1
depth=0 CN = localhost
verify return:1
---
Certificate chain
 0 s:/CN=localhost
   i:/CN=localhost
---
Server certificate
-----BEGIN CERTIFICATE-----
MIICBjCCAW+gAwIBAgIEUZgvXTANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjIwMjA3MTc1MDAyWhcNMjMwMjA3MTc1MDAyWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBALEL2U4H
H7ZFM4QIMIX/E/RGL/5blcIyjSb+0rBHM455A+TknHIFfI38XHEBXZjxZlNeEdZE
POJmxCb85TLGDZGkf8DkwSldmTQn5wKFJ+4oT/NhZdXgKfOEn6PQ7pa/HqG7gzmq
lilyov9G1IG1xL/JUKMO7HVTqgZyu0zZu+kTAgMBAAGjZTBjMBQGA1UdEQQNMAuC
CWxvY2FsaG9zdDBLBglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0
ZWQgYnkgTmNhdC4gU2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3
DQEBBQUAA4GBAEL/Io/djIdtnBpc+JbrjPaV8xRnBqB1ZD4LtrPQObXXBdWe5i9j
v7k/p4e6YY0S0/qCqLhpAHKHUWmpTxsBGFebLenGHclpcmANG79Bf4gdWCeSOAYm
CqaCPR5NW4Inf5fHx0seQtRwzAJkUBbPxgHXPim5Dcgn+gYuY/Dl4zOw
-----END CERTIFICATE-----
subject=/CN=localhost
issuer=/CN=localhost
---
No client certificate CA names sent
Peer signing digest: SHA512
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1019 bytes and written 269 bytes
Verification error: self signed certificate
---
New, TLSv1.2, Cipher is ECDHE-RSA-AES256-GCM-SHA384
Server public key is 1024 bit
Secure Renegotiation IS supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
SSL-Session:
    Protocol  : TLSv1.2
    Cipher    : ECDHE-RSA-AES256-GCM-SHA384
    Session-ID: 04DB598779446BDA6D3360923C6A530FAFBF29FF4E7A0A1E33D7120177119429
    Session-ID-ctx: 
    Master-Key: 71A6996D3428BA4F6A7F51F0C569DA65F5836BC08E6D68C2A2561DA4B68E8E706115F8561FF87D1EF797CF182335082A
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - cc 16 e1 c4 9e 72 74 8d-e3 d2 a1 30 e3 7a e2 a5   .....rt....0.z..
    0010 - 89 7c f4 45 b0 ab 37 b2-fd 98 a8 e6 df 04 52 52   .|.E..7.......RR
    0020 - bb 0d 50 76 eb 79 d3 0f-3c ab 99 c2 c1 4c da 22   ..Pv.y..<....L."
    0030 - c2 84 7d 19 0d 09 dd b6-91 68 4e b7 97 77 ff ed   ..}......hN..w..
    0040 - 16 71 4f 2c b3 41 a7 aa-b5 79 73 af bd 78 30 7f   .qO,.A...ys..x0.
    0050 - 35 2a 8f a9 6e cb b6 17-4b 45 d7 70 72 ff f9 ab   5*..n...KE.pr...
    0060 - 36 fb 45 c5 69 42 44 a6-60 5d 6c d9 53 32 92 5f   6.E.iBD.`]l.S2._
    0070 - bd bf 15 ba 28 fd 16 c4-c3 8c d0 31 bc fa e5 71   ....(......1...q
    0080 - 05 9c 3e 6d fb c2 e9 19-31 8c bf c0 7c c5 6d b6   ..>m....1...|.m.
    0090 - 97 38 0c db cf f4 a1 6e-e8 1c 28 64 eb 5e 07 af   .8.....n..(d.^..

    Start Time: 1645745876
    Timeout   : 7200 (sec)
    Verify return code: 18 (self signed certificate)
    Extended master secret: yes
---
cluFn7wTiGryunymYOu4RcffSxQluehd
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$ 


``` 
---
## Notas adicionales
Guardar llave privada y cambiar los permisos.
```  shell
angel@angelMnt:~$ nano /tmp/private_key
angel@angelMnt:~$ chmod 400 /tmp/private_key
``` 

Conenctarse con la llave privada y obtener contraseña.
```shell
angel@angelMnt:~$ ssh -i /tmp/private_key bandit17@bandit.labs.overthewire.org -p 2220
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$ 
```


#### Comandos linux

**nmap** permite realizar un escaneo a los puertos.
**-p** Indicar el rango de puertos a escanear.

**chmod 400**  
Cambiar los permisos a un archivo o directorio, el primer número es para el usuario, el segundo es el de grupo y el tercero otros usuarios.
**4** Lectura 
**2** Escritura
**3** Ejecutar

---
## Referencias
https://www.redeszone.net/tutoriales/configuracion-puertos/nmap-escanear-puertos-comandos/

http://web.mit.edu/rhel-doc/3/rhel-sg-es-3/s1-server-ports.html

https://en.wikipedia.org/wiki/Port_scanner

https://www.hostinger.mx/tutoriales/cambiar-permisos-y-propietarios-linux-linea-de-comandos/