# PW Crack 1

---
## Objectivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/52/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/52/level1.flag.txt.enc) in the same directory too.


---
## Solución
``` bash
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls
level1.flag.txt.enc  level1.py
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat level1.flag.txt.enc 
A
 Rr1w�Q	nVT_nPRVWangel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat level1.
cat: level1.: No such file or directory
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat level1.py 
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


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "1e1a"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 level1.py 
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 


```
### `picoCTF{545h_r1ng1ng_fa343060}`
---
## Notas adicionales

---
## Referencias
