---
description: Nell'ambito di linguaggi utilizzati per lo sviluppo di applicazioni locali
---

# Funzioni Rientranti

### Definizione

> Una funzione si dice **rientrante** se, in seguito alla sua esecuzione, lo stato non è alterato.  
> **Non rientrante** è quindi una funzione che, quanto terminata, vede lo stato modificato.

{% code title="Definizione della funzione errore come rientrante" %}
```c
#include <errno.h>

int errore(char *msg, int errCode) {
    printf("ERROR: %s with code %d", msg, errCode);
    printf("%s, %d", strerror(errno), errno);
    return errCode;
}
```
{% endcode %}

{% code title="Porzione di codice che NON modifica lo stato dell\'applicazione" %}
```c
int rc;

if(argc != 3) {
    rc = errore("USAGE: FILE_NAME P1 P2", -1);
    return rc;
}
```
{% endcode %}

{% code title="Definizione della funzione come NON rientrante" %}
```c
include <errno.h>

void errore(char *msg, int errCode) {
    printf("ERROR: %s with code %d", msg, errCode);
    printf("%s, %d", strerror(errno), errno);
    exit(errCode);
}
```
{% endcode %}

{% code title="Porzione di codice che modifica lo stato dell\'applicazione" %}
```c
if(argc != 3) {
    errore("USAGE: FILE_NAME P1 P2", -1);
}
```
{% endcode %}

### Funzioni Ricorsive

Per definizione, una funzione ricorsiva sarà sempre rientrante.

```c
int fib(n) {
    if(n == 0 || n == 1)
        return 0;
    
    /* 
        Non è possibile, ad esempio, sostituire la return con una exit,
        in quanto impediremmo l'esecuzione ricorsiva stessa
    */
    return fib(n - 1) + fib(n - 2) 
}
```

### \(OT\) Stack e Heap

Lo _stack_ e lo _heap_ sono contenuti in memoria centrale e si evolvono in direzione opposta. 

Lo stack cresce dall'alto verso il basso, lo heap dal basso verso l'alto. 

Nei linguaggi ad alto livello, è il compilatore a sincerarsi che i due non vadano a strabordare l'uno nell'area di memoria dell'altro. In ambienti più a basso livello \(E.G. Assembler\) è nostro compito effettuare le debite verifiche.

