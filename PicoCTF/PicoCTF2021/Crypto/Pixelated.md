### Pixelated

---
## Objectivo
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/e8054e22552c6aba591cdf7440eb25e4/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/e8054e22552c6aba591cdf7440eb25e4/scrambled2.png)

---
## Solución
``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ python3 junta_imagen.py 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls
junta_imagen.py  result.png  scrambled1.png  scrambled2.png  values
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ cat junta_imagen.py 
import numpy as np
from PIL import Image

# Open images
im1 = Image.open("scrambled1.png")
im2 = Image.open("scrambled2.png")

# Make into Numpy arrays
im1np = np.array(im1)
im2np = np.array(im2)

# Add images
result = im2np + im1np
# Convert back to PIL image and save
Image.fromarray(result).save('result.png')
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 

```

### picoCTF{d72ea4af}

---
## Notas adicionales

---
## Referencias

https://picoctf2021.haydenhousen.com/cryptography/pixelated
