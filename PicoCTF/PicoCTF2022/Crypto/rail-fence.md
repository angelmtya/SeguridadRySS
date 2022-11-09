# rail-fence
---
## Objectivo
A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it?Download the message [here](https://artifacts.picoctf.net/c/272/message.txt).Put the decoded message in the picoCTF flag format, `picoCTF{decoded_message}`.

---
## Solución

Ta _7N6DDDhlg:W3D_H3C31N__0D3ef sHR053F38N43D0F i33___NA

```
T.....a.....*....._.....7.....N.....6.....D.....D.....D.....
.h...l.g...:.W...3.D..._.H...3.C...3.1...N._..._.0...D.3...
..e.f...*.s...H.R...0.5...3.F...3.8...N.4...3.D...0.F...
...*.....i.....3.....3....._....._....._.....N.....A
```
### the flag is: WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_D00AFDD3


---
## Notas adicionales
**Rail fence**

 el texto sin formato se escribe en diagonal hacia abajo en "rieles" sucesivos de una cerca imaginaria, luego se mueve hacia arriba cuando se alcanza el riel inferior, hacia abajo nuevamente cuando se alcanza el riel superior, y así sucesivamente hasta que se escribe todo el texto sin formato. fuera. Luego, el texto cifrado se lee en filas.


---
## Referencias
https://en.wikipedia.org/wiki/Rail_fence_cipher