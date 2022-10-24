
# Enhance!

---
## Objectivo

Download this image file and find the flag.

-   [Download image file](https://artifacts.picoctf.net/c/137/drawing.flag.svg)

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat caxcan-club.py 
def roll(text):
    return text[::-1]

def swoop(text):
    text = list(text)
    for i in range(len(text)):
        if text[i] not in '{}':
            text[i] = chr(ord(text[i]) - (i % 6))
    return ''.join(text)

password = input("Enter the password: ")
if swoop(roll(password)) == "}zudidsbybwxaqaqehxbebimt`jks{XNidpk":
	print("Welcome in!")
else:
    print("Sorry, wrong password.")
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat pruebas.py 
def roll(text):
    return text[::-1]


def swoop(text):
    text = list(text)
    for i in range(len(text)):
        if text[i] not in '{}':
            text[i] = chr(ord(text[i]) + (i % 6))
    return ''.join(text)

# roll(texto)

def swoop2(text):
    text = list(text)
    for i in range(len(text)):
        if text[i] not in '{}':
            text[i] = chr(ord(text[i]) - (i % 6))
    return ''.join(text)

texto = input()
print(roll(swoop2(texto)))


angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 pruebas.py
}zudidsbybwxaqaqehxbebimt`jks{XNidpk
flagMX{ohh_the_caxcan_pass_was_easy}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 

```

## `flagMX{ohh_the_caxcan_pass_was_easy}`


---
## Notas adicionales

### Comandos linux

**inkscape**
Editor de diseño grafico.

**SVG** es un lenguaje usado para dibujar y representar gráficos, imágenes y logotipos, o sea que son gráficos que pueden manipularse con CSS y JavaScript.


---
## Referencias

https://es.wikipedia.org/wiki/Gr%C3%A1ficos_vectoriales_escalables