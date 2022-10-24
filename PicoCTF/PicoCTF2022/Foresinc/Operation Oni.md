# Operation Oni

---
## Objectivo
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

-   [Download disk image](https://artifacts.picoctf.net/c/372/disk.img.gz)
-   Remote machine: `ssh -i key_file -p 51905 ctf-player@saturn.picoctf.net`

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ ls
disk.img  disk.img.gz
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ fls -o 206848 disk.img
d/d 11:	lost+found
d/d 12:	boot
d/d 13:	etc
d/d 79:	proc
d/d 80:	dev
d/d 81:	tmp
d/d 82:	lib
d/d 85:	var
d/d 94:	usr
d/d 104:	bin
d/d 118:	sbin
d/d 458:	home
d/d 464:	media
d/d 468:	mnt
d/d 469:	opt
d/d 470:	root
d/d 471:	run
d/d 473:	srv
d/d 474:	sys
V/V 33049:	$OrphanFiles
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ fls -o 206848 disk.img 3916
r/r 2345:	id_ed25519
r/r 2346:	id_ed25519.pub
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ icat -o 206848 disk.img 2345 > k.key
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ chmod 400 k.key 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ ssh -i k.key -p 54204 ctf-player@saturn.picoctf.net
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 5.13.0-1025-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt 
picoCTF{k3y_5l3u7h_339601ed}ctf-player@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/tmp2$ 


```


---
## Notas adicionales

#### Comandos linux 

**chmod 400 k.key** Cambiar los permisos de la clave

**mmls**
muestra el diseño de partición de un sistema de volumen

**icat**
genera el contenido de un archivo en función de su número de inodo.

---
## Referencias

https://github-wiki-see.page/m/not1cyyy/CTF-Writeups/wiki/picoCTF-%3A-Operation-Oni