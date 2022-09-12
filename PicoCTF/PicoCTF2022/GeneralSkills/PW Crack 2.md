# PW Crack 2

---
## Objectivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level2.flag.txt.enc) in the same directory too.

---
## Solución
``` bash

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls
level2.flag.txt.enc  level2.py
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nano level2.py 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat level2.py 
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level2.flag.txt.enc', 'rb').read()



def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_2_pw_check()
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3
Python 3.8.10 (default, Jun 22 2022, 20:18:18) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)
'39ce'
>>> exit()
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 level2.py 
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 


```

### `picoCTF{tr45h_51ng1ng_502ec42e}`
---
## Notas adicionales

---
## Referencias
