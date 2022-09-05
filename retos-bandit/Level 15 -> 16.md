# Level 15 -> 16
---
## Objectivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

---
## Datos de acceso
- user -> **bandit15**
- Passwor -> jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
- host ->  **bandit.labs.overthewire.org**
- port -> **2220**

---
## Solución
``` shell
bandit15@bandit:~$ openssl s_client -connect localhost:30001
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
MIICBjCCAW+gAwIBAgIEZOzuVDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjEwOTMwMDQ0NTU0WhcNMjIwOTMwMDQ0NTU0WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM9En7CC
uPr6cVPATLAVhWMU1hggfIJEp5sZN9RPUbK0zKBv802yD54ObHYmIge6lqqkgXOz
2AuI4UfCG4iMb0UYUCA/wISwNqUQrjcja0OnqzCTRscXzzoIsHbC8lGFzMDRz3Jw
8nBD6/2jvFt1rnBtZ4ghibNn5rFHRi5EC+K/AgMBAAGjZTBjMBQGA1UdEQQNMAuC
CWxvY2FsaG9zdDBLBglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0
ZWQgYnkgTmNhdC4gU2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3
DQEBBQUAA4GBAD7/moj14DUI6/D6imJ8pQlAy/8lZlsrbyRnqpzjWaATShDYr7k3
umdRg+36MciNFAglE7nGYZroTSDCm650D81+797owSXLPAdp1Q6JfQH5LOni2kbw
UHcO9hwQ+rJzEgIlfGOic7dC5lj8DBU5tugY87RZGKiZ2GG77WXas9Iz
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
    Session-ID: 7CD98D36B30D2AC640384C48FD095103841087AD8CEF72C1DA27F41A535E2C19
    Session-ID-ctx: 
    Master-Key: 8EAD090A7585F0C2647EB4B0CF79D1142B55944CC6E340065A4E1C680985C78DDE65D14521B5F3FC682514CBE9DDFF81
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 8a eb e8 f5 31 15 46 ad-b2 a8 10 c1 51 b9 66 14   ....1.F.....Q.f.
    0010 - be e9 31 26 97 8e 60 16-eb 32 dc 0c f3 d1 0c c1   ..1&..`..2......
    0020 - 2b f2 da d5 cc 4c a3 6b-60 e3 cf 77 bd e0 c9 cf   +....L.k`..w....
    0030 - 2a fa 0a 48 7e 72 be 87-29 f3 dd af 23 3b 47 ce   *..H~r..)...#;G.
    0040 - 33 f5 1f cd 16 45 c2 7c-df 88 7d ba d2 bd 22 fe   3....E.|..}...".
    0050 - fd 64 a2 5b c1 e7 54 2b-d6 46 fc 8c 71 1a 25 76   .d.[..T+.F..q.%v
    0060 - 6d 3e 52 ce 00 fa 87 cc-43 9e 8d 91 ba 78 1f 51   m>R.....C....x.Q
    0070 - 86 1e e5 47 29 09 ca cf-ea cb 52 31 f9 24 fa aa   ...G).....R1.$..
    0080 - 3f 8d 9e 3e a8 16 0f 73-ba 03 2d 7c 00 2e cd a5   ?..>...s..-|....
    0090 - ea 92 98 a3 d1 1f 0d 54-3c e1 59 22 93 5f b1 dc   .......T<.Y"._..

    Start Time: 1645742769
    Timeout   : 7200 (sec)
    Verify return code: 18 (self signed certificate)
    Extended master secret: yes
---
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt         
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed

``` 
---
## Notas adicionales

**Certificados SSL/TLS de servidor web**
Estos certificados le permitirán establecer comunicaciones con sus clientes utilizando la tecnología SSL o TLS, los estándares para comunicaciones seguras en la Web. Su servidor se identificará a los clientes con el nombre del dominio donde se encuentra su servicio Web, además de garantizar la integridad y confidencialidad de las comunicaciones.

#### Comandos linux

**openssl**
Para crear, convertir, gestionan los Certificados SSL, viene con una herramienta de cliente que puede usar para conectarse a un servidor seguro.
**-connect** Interruptor se usa para establecer la conexión TCP.
**s_client** Herramienta configura el nombre de host enviado en el nivel TLS


---
## Referencias

https://geekflare.com/es/openssl-commands-certificates/

https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html

https://www.cert.fnmt.es/catalogo-de-servicios/certificados-electronicos/certificado-servidor#:~:text=El%20certificado%20de%20servidor%20est%C3%A1ndar,la%20mayor%C3%ADa%20de%20los%20casos.