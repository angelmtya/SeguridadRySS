# Tab, Tab, Attack

---
## Objectivo

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: Addadshashanammu.zip

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ unzip Addadshashanammu.zip 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ ls -R Addadshashanammu/
Addadshashanammu/:
Almurbalarammi

Addadshashanammu/Almurbalarammi:
Ashalmimilkala

Addadshashanammu/Almurbalarammi/Ashalmimilkala:
Assurnabitashpi

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi:
Maelkashishi

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi:
Onnissiralis

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis:
Ularradallaku

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku:
fang-of-haynekhtnamet
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/Addadshashanammu$ strings  Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet | grep pico
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_2bcfb2ab}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/Addadshashanammu$ 
```
### `picoCTF{l3v3l_up!_t4k3_4_r35t!_2bcfb2ab}`


---
## Notas adicionales

### Comandos linux

**unzip**
Descomprimir un archivo zip.

---
## Referencias
https://kinsta.com/es/base-de-conocimiento/descomprimir-archivo-zip/#paso-3--descomprimir-el-archivo-zip-usando-la-terminal