## The Numbers

---
## Objectivo

The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat thenumbers.py 
entrada = input().split()
alfabeto = {'1':'a','2':'b','3':'c','4':'d','5':'e','6':'f','7':'g','8':'h','9':'i','10':'j','11':'k','12':'l','13':'m','14':'n','15':'o','16':'p','17':'q','18':'r','19':'s','20':'t','21':'u','22':'v', '23':'w','24':'x','25':'y','26':'z'}

cadena=''

for c in entrada:
	a = alfabeto.get(c)
	if(a!=None):
		cadena+=a
	else:
		cadena+=c

print(cadena.upper())
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nano thenumbers.py
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 thenumbers.py 
16 9 3 15 3 20 6 { 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14 }
PICOCTF{THENUMBERSMASON}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 

```

### `PICOCTF{THENUMBERSMASON}`

---
## Notas adicionales



---
## Referencias


	