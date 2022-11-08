## Mind your Ps and Qs

---
## Objectivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/2604f8b51a5cc62d38a3736938f19cef/values)
Decrypt my super sick RSA:
c: 861270243527190895777142537838333832920579264010533029282104230006461420086153423
n: 1311097532562595991877980619849724606784164430105441327897358800116889057763413423
e: 65537

---
## Solución
``` bash
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat values 
Decrypt my super sick RSA:
c: 861270243527190895777142537838333832920579264010533029282104230006461420086153423
n: 1311097532562595991877980619849724606784164430105441327897358800116889057763413423
e: 65537angel
@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3
Python 3.8.10 (default, Jun 22 2022, 20:18:18) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> >>> c = 861270243527190895777142537838333832920579264010533029282104230006461420086153423
>>> e = 65537
>>> p = 1955175890537890492055221842734816092141
>>> q =  670577792467509699665091201633524389157003
>>> n = p * q
>>> n
1311097532562595991877980619849724606784164430105441327897358800116889057763413423
>>> tn = (p-1)*(q-1)
>>> d = inverse(e,tn)
>>> m = pow(c,d,n)
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_13686679}'
>>> 




```

### `picoCTF{sma11_N_n0_g0od_13686679}

---
## Notas adicionales



---
## Referencias


https://www.youtube.com/watch?v=pwGSp_4YHTg&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=44&ab_channel=hackadvisermx