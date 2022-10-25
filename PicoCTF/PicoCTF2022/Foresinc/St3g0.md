### St3g0

---
## Objectivo
Download this image and find the flag.

-   [Download image](https://artifacts.picoctf.net/c/423/pico.flag.png)

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/image-stego-tool$ ls
pico.flag.png  README.md  stego.py  stego-start.png
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/image-stego-tool$ python3 stego.py
--Welcome to $t3g0--
1: Encode
2: Decode
2
Enter Source Image Path
./pico.flag.png
Decoding...
Hidden Message: picoCTF{7h3r3_15_n0_5p00n_a9a181eb}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/image-stego-tool$ 

```


---
## Notas adicionales

### Comandos linux
  **mmls** - Display the partition layout of a volume system  (partition tables)

---
## Referencias

http://manpages.ubuntu.com/manpages/trusty/man1/mmls.1.html
