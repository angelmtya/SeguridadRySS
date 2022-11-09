
### basic-mod2

---
### Objectivo

A new modular challenge! Take each number mod 41 and find the modular inverse for the result. Then map to the following character set: 1-26 are the alphabet, 27-36 are the decimal digits, and 37 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. picoCTF{decrypted_message})

---
### Solución
``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat message.txt 
104 290 356 313 262 337 354 229 146 297 118 373 221 359 338 321 288 79 214 277 131 190 377 angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat mod2.py 

def find_mod_inv(a,m):

    for x in range(1,m):
        if((a%m)*(x%m) % m==1):
            return x
    raise Exception('The modular inverse does not exist.')

a = [ 104, 290, 356, 313, 262, 337, 354, 229, 146, 297, 118, 373, 221, 359, 338, 321, 288, 79, 214, 277, 131, 190, 377]
m = 41

try:
	for i in a:
		res=find_mod_inv(i,m)
		print(str(res),end=" ")

except:
    print('The modular inverse does not exist.')
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 mod2.py 
28 14 22 30 18 32 30 12 25 37 8 31 18 4 37 35 1 27 32 4 36 30 36 angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 



```

35 1 27 32 4 36 30 36 
 8  a  0   5  d  9   3    9

### picoCTF{1NV3R53LY_H4RD_8a05d939}

---
### Notas adicionales

---
### Referencias

https://github.com/arvindshima/PicoCTF-2022/blob/main/Cryptography/basic-mod2.md

