# Search source

---
## Objectivo

The developer of this website mistakenly left an important artifact in the website source, can you find it?The website is [here](http://saturn.picoctf.net:61941/)


---
## Solución
```sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ curl http://saturn.picoctf.net:61941/css/style.css | strings | grep picoCTF
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 10449  100 10449    0     0  25610      0 --:--:-- --:--:-- --:--:-- 25547
/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7} **/
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/S2/tmp$ 

```
### `picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7}`

---
## Notas adicionales


---
## Referencias

picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
