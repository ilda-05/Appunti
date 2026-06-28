
Un indirizzo di memoria è un identificatore univoco di un certo posto nella memoria, dove componenti hardware o software possono andare a leggere, scrivere o modificare dati.

Gli indirizzi di memoria sono nella maggior parte dei casi sono in esadecimale.
Esempi : 

- 0x000000BC89BFFDFC
- 0x00000037225FFABC

Sono presenti due tipi di indirizzi di memoria, **fisico e virtuale**.

Esempio di programma in C che visualizza l'indirizzo in memoria di due variabili :

```c
#include<stdio.h>

int main(){

    int num1 = 15;
    int num2 = 20;

    // NOTA: il tipo della variabile puntatore deve coincidere con la variabile a
    // cui punta

	// Stampa gli indirizzi di memoria 
    printf("%p\n",&num1); 
    printf("%p\n",&num2);
    return 0;
    
}
```

Output:
```bash
00000018EF7FFC4C
00000018EF7FFC48
```

![[memory_address.excalidraw]] 
