
**La velocità è il rapporto tra lo spazio percorso e il tempo impiegato.**

$$ v = \frac{s}{t}$$
v = Velocità
s = Spazio
t = Tempo

Esempio in C :

```c
#include<stdio.h>

int main(){

    float spazio, tempo, velocita;
    
    spazio = 150; // metri
    tempo = 4; // secondi

    velocita = spazio/tempo;

    printf("Spazio: %.2f metri\n", spazio);
    printf("Tempo: %.2f secondi\n", tempo);
    printf("Velocita': %.2f m/s\n", velocita);

}
```

Output : 

```
Spazio: 150.00 metri
Tempo: 4.00 secondi
Velocita': 37.50 m/s
```

###### Velocità Angolare

La velocità angolare si calcola facendo :

$$\omega=\frac{2\pi}{T}$$
Oppure :

$$\omega=2\pi f$$

Dove :

T = periodo ( il tempo per un giro completo)
f = frequenza ( giri al secondo )


###### Velocità Tangenziale

La velocità tangenziale si calcola :

$$ v = \omega \cdot r$$
Dove :

v = Velocità tangenziale.
$\omega$ = Radianti al secondo.
r = Raggio.