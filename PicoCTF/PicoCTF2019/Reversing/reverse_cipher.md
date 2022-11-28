# reverse_cipher
---
## Objectivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this). Can you reverse the flag.

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2019/Reversing$ cat exp.py 
import os
import mmap

def memory_map(filename, access=mmap.ACCESS_READ):
    size = os.path.getsize(filename)
    fd = os.open(filename, os.O_RDONLY)
    return mmap.mmap(fd, size, access=access)

with memory_map("rev_this") as bin_file:
    for i in range(8):
        print(chr(bin_file[i]), end = '')
    for i in range(8, 23):
        if (i & 1) == 0:
            print(chr(bin_file[i] - 5), end = '')
        else:
            print(chr(bin_file[i] + 2), end = '')
    print (chr(bin_file[23]))
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2019/Reversing$ 

```

### `picoCTF{r3v3rs36ad73964}


---
## Notas adicionales


**Ghidra**
Ghidra es un marco de ingeniería inversa de software sofisticado, multiplataforma y de código abierto que ofrece herramientas de grado militar para analizar y revertir archivos binarios de software. Con Ghidra, puede realizar ingeniería inversa o descompilar un software binario y estudiar el código fuente que se encuentra debajo.


---
## Referencias

https://www.intel.com/content/dam/develop/external/us/en/documents/introduction-to-x64-assembly-181178.pdf