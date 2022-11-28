# unpackme.py

---
## Objectivo
Can you get the flag?Reverse engineer this [Python program](https://artifacts.picoctf.net/c/466/unpackme.flag.py).

---
## Solución
``` bash
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls
unpackme.flag.py
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nano unpackme.flag.py 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat unpackme.flag.py 
import base64
from cryptography.fernet import Fernet



payload = b'gAAAAABiMD09KmaS5E6AQNpRx1_qoXOBFpSny3kyhr8Dk_IEUu61Iu0TaSIf8RCyf1LJhKUFVKmOt2hfZzynRbZ_fSYYN_OLHTTIRZOJ6tedEaK6UlMSkYJhRjAU4PfeETD-8gDOA6DQ8eZrr47HJC-kbyi3Q5o3Ba28mutKCAkwrqt3gYOY9wp3dWYSWzP4Tc3NOYWfu-SJbW997AM8GA-APpGfFrf9f7h0VYcdKOKu4Vq9zjJwmTG2VXWFET-pkF5IxV3ZKhz36L5IvZy1dVZXqaMR96lovw=='

key_str = 'correctstaplecorrectstaplecorrec'
key_base64 = base64.b64encode(key_str.encode())
f = Fernet(key_base64)
plain = f.decrypt(payload)
print(plain.decode())
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 unpackme.flag.py 

pw = input('What\'s the password? ')

if pw == 'batteryhorse':
  print('picoCTF{175_chr157m45_85f5d0ac}')
else:
  print('That password is incorrect.')


angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 


```

---
## Notas adicionales

---
## Referencias
