Un thread **è la parte più piccola di esecuzione** che può essere gestita in un sistema operativo.

Uno o più thread si trovano all'interno di un processo, e possono anche condividere alcune delle loro risorse.

Esempio di un solo thread in un processo.
```cpp
#include<iostream>

int main(){
    std::cout<<"Thread del main";
}
```

Esempio di due thread in un processo.
```c++
#include<iostream>
#include<thread>

void another_thread(){
    std::cout<<"Sono un'altro thread generato da "<<__func__<< "\n" ;
}

int main(){
    std::thread t1(another_thread);
    t1.join(); //Il thread del main aspetta
    std::cout<<"Thread del main"<<"\n";
}
```


Quando più thread vengono eseguiti contemporaneamente, si chiama multithreading. 

I thread hanno 3 stati :
- **Running**
	Thread che in quel momento è in esecuzione, sta girando.
- **Blocked**
	Il thread entra in un stato di blocco, dove non può svolgere nessun compito, e non fa uso della cpu, in attesa di un determinato evento. 
	Nel caso del secondo esempio, il main ha aspettato che un altro thread finisse di svolgere il suo compito, e poi è partito.
- **Ready**
	Quando un thread è pronto a essere selezionato ad essere eseguito, ma non lo è ancora.
- **Terminated**
	Quando un thread ha finito di svolgere il suo compito ed è stato terminato.

**Più thread possono essere eseguiti in parallelo.**

![[process_threads.excalidraw]]

Un uso che se ne può fare, per esempio, è di avere più thread per fare più azioni contemporaneamente, molto semplicemente, un thread che si occupa di aumentare un contatore ogni secondo, e un altro thread che si occupa magari di stampare ogni secondo la parola "Hello", e un altro thread che anche esso ogni secondo stampa "World!".

Esempi di thread che vengono eseguiti in parallelo.
```cpp
#include<iostream>
#include<thread>

void print_hello_thread(){
    for (int i = 0; i < 10; i++)
        std::cout<<"Hello ";
}

void print_world_thread(){
    for (int i = 0; i < 10; i++)
        std::cout<<"World!";
}

int main(){ 
    std::thread t1(print_hello_thread);
    std::thread t2(print_world_thread);

    t1.join();
    t2.join();
}
```

Output :
```bash
Output 1:
Hello Hello Hello Hello World!Hello World!World!World!World!World!World!Hello Hello World!World!Hello Hello World!Hello

Output 2:
Hello Hello World!World!World!Hello World!World!World!World!World!World!World!Hello Hello Hello Hello Hello Hello Hello

Output 3:
Hello Hello Hello Hello Hello Hello World!Hello World!Hello Hello Hello World!World!World!World!World!World!World!World!
```

L'output non è mai uguale, le parole Hello e World sono mischiati, perché vengono stampate in parallelo.

