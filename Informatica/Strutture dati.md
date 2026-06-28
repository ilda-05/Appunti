---
tags:
  - informatica
---

Nella programmazione ci sono diversi tipi di strutture dati :



## Array 

Un array è un contenitori di più dati all'interno, a cui ci si può accedere usando l'indice di dove si trova il dato.

Solitamente ha una dimensione fissa.

![[array.excalidraw]]

Esempio di inizializzazione di un array:
```c
#include<stdio.h>

int main(){

    int numbers[5] = {1,5,7,3,6}; // Qui inizializziamo l'array
								  // di dimensione 5
    
    /*
	* Ciclo for che itera per 5 volte stampando ogni valore contenuto all'interno
    */
    for(int i = 0; i < 5; i++)
        printf("%d\n",numbers[i]);
        
    return 0;

}
```
Output: 
```bash
1
5
7
3
6
```

Ha una velocità di accesso agli elementi di O(1).
## Linked List

Una linked lista ( o lista concatenata ) è una lista di dati lineare, dove ogni nodo contiene dei dati e un riferimento (puntatore) al nodo successivo.

![[linked_list.excalidraw]]

Ha una velocità di accesso agli elementi di O(n).

I nodi non sono salvati in memoria in modo contiguo.
## Stack

Struttura di dati a "pila".

Ogni dato che viene inserito viene inserito come ultimo, in cima, e ogni che viene rimosso un elemento, viene rimosso solo l'ultimo elemento.

![[stack_structure.excalidraw]]

Può avere una velocitò di O(1) o O(n), dipende a quale dato si vuole accedere e cosa si vuole fare.

Può diventare O(n) nel caso non si volesse accedere a un dato che non sia l'ultimo, ma per esempio a un dato che si trova in mezzo, in quel caso, andrebbero rimossi tutti gli elementi fino a che non si arriva a quel elemento lì.
