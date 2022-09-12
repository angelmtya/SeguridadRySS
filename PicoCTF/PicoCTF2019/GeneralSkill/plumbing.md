# plumbing

---
## Objectivo

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.

---
## Solución

``` shell
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ nc jupiter.challenges.picoctf.org 14291 | grep pico
picoCTF{digital_plumb3r_ea8bfec7}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 

```

### `picoCTF{digital_plumb3r_ea8bfec7}`

---
## Notas adicionales

#### Comandos linux

**/   >**
La redirección es la transferencia de la salida estándar a algún otro destino, como otro programa o archivo.

---
## Referencias

linfo.org/pipes.html