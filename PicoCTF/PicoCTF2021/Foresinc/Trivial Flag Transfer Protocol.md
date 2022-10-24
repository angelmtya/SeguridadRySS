Trivial Flag Transfer Protocol
---
## Objectivo

Figure out how they moved the [flag](https://mercury.picoctf.net/static/ed308d382ae6bcc37a5ebc701a1cc4f4/tftp.pcapng).

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ ls
instructions.txt  picture1.bmp  plan  program.deb  tftp.pcapng
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ cat instructions.txt | tr [A-Z] [N-ZA-M] > texto1
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ nano texto1 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ cat texto1 
TFTP DOESNT ENCRYPT
OUR
TRAFFIC
SOWE
MUST
DISGUISE OUR FLAG TRANSFER.FIGURE OUT A WAY TO HIDE THE FLAG
AND I WILL CHECK BACK FOR THE PLAN
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ nano texto2
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ cat texto2
I
USED THE PROGRAM AND HID IT WITH- DUEDILIGENCE .CHECK OUT THE PHOTOS
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ sudo apt-get install steghide
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ steghide --extract -sf picture1.bmp 
Anotar salvoconducto: 
steghide: �no pude extraer ning�n dato con ese salvoconducto!
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ steghide --extract -sf picture1.bmp 
Anotar salvoconducto: 
steghide: �no pude extraer ning�n dato con ese salvoconducto!
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ steghide --extract -sf picture2.bmp 
Anotar salvoconducto: 
steghide: �no pude extraer ning�n dato con ese salvoconducto!
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ steghide --extract -sf picture3.bmp 
Anotar salvoconducto: 
anot� los datos extra�dos e/"flag.txt".
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2021/Forensics/tftp$ cat flag.txt 
picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}

	 


```

---
## Notas adicionales
**steghide** 
es una herramienta que puede servirnos para practicar la esteganografía.
**--extract**  extraer archivos.
**-sf**  elegir archivo stego


---
## Referencias
https://www.linuxadictos.com/steghide-esteganografia-para-ocultar-texto-en-imagenes.html