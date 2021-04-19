# Sistema Distribuito

> E' un sistema costituito da un insieme di applicazione logicamente indipendenti, che collaborano tra loro per portare avanti obiettivi comuni.
>
> Queste applicazioni logiche comunicano tra loro attraverso sistemi di comunicazione hardware e software.

### Ruoli \(o personaggi\)

* **Client:** l'utilizzatore del sistema
* **Server:** il fornitore del servizio
* **Attore:** entità che a seconda dei casi assume la funzione di client o di server

{% hint style="danger" %}
I ruoli dei sistemi distribuiti **sono processi**, non componenti dell'host
{% endhint %}

### Proprietà

* **Affidabilità**: capacità del sistema di adattarsi ad eventuali malfunzionamenti e di riuscire a continuare a funzionare
* **Integrazione:** capacità del sistema di interagire con nuovi dispositivi all’interno di esso, sia che siano nuovi dispositivi, sia che siano obsoleti.
* **Trasparenza:** capacità del sistema di mostrarsi all’utente come un unico dispositivo / nodo / elemento. Si suddivide in:
  * **Trasparenza d'accesso:** permette di accedere alla risorsa nascondendo all'utente finale eventuali differenze nella modalità di accesso alla rete da parte dell'utento
  * **Trasparenza di locazione:** all'utente non deve interessare il luogo di fisica locazione della risorsa
  * **Trasparenza di replicazione:** possibilità del sistema di duplicare le risorse senza impattare sull'esperienza finale dell'utente
  * **Trasparenza ai guasti:** il sitema maschera un eventuale guasto e la relativa procedura di recovery
  * **Trasparenza di migrazione:** la possibilità di trasferire logicamente o fisicamente una risorsa
  * **Trasparenza di prestazione:** il sistema può scalare a seconda delle necessità dell'utente
  * **Trasparenza di scalabilità:** il sistema può essere espanso senza interrompere o modificarne il funzionamento

### Vantaggi

* **Economicità**
* **Apertura:** presupponendo l'utilizzo di protocolli standard, questo tipo di sistema presenta tre tipi di apertura.
  * **Interoperabilità:** la possibilità di operare su diversi sistemi diversi giungendo sempre allo stesso risultato
  * **Portabilità:** la possibilità di utilizzare una data risorsa su piattaforme diverse
  * **Ampliabilità:** la facilità nell'espendere il sistema con nuove componenti, siano queste hardware o software
* **Connettività e collaborazione:** la possibilità di condividere una risorsa e di poter creare inoltre gruppi di lavoro per lo svolgimento di determinate attività
* **Prestazioni e scalabilità:** la possibilità di aumentare il sistema. A seconda della potenza di calcolo richiesta, si avrà un sistema che presenta una densità di nodi più o meno alta. Esistono due tipi di scalabilità.
  * **Scalabilità verticale:** aggiornamento di determinate componenti per migliorare le prestazioni
  * **Scalabilità orizzontale:** incremento della molteplicità delle macchine
* **Tolleranza ai guasti:** il sistema, data la ridondanza di nodi che lo caratterizzaè in grado di nascondere all'utente finale eventuali guasti.

### Svantaggi

* **Produzione software:** la difficoltà nel produrre software nei sistemi distribuiti. Si è superata grazie a tre principali evoluzioni:
  * Definizione dello stack TCP/IP
  * Sviluppo delle architetture web e dei relativi linguaggi
  * Sviluppo del linguaggio Java, che con la sua JVM consente di eseguire lo stesso applicativo su macchine differenti
* **Complessità:** essendo il sistema basato su più risorse, è necessario disporre di un'architettura hardware e software per l'interconnessione dei diversi host. E' altresì complesso valutare le prestazioni in quanto non tutti i nodi lavorerranno sempre al 100%.
* **Sicurezza:** in quanto sistemi idealmente accessibili a chiunque, si presenta la necessità di proteggerli implementando sistemi di autenticazione e autorizzazione quali l'utilizzo di credenziali username/password, token o simili.
* **Comunicazione:** la necessità di definire i protocolli di comunicazione. L'interfaccia hardware \(i.e. la rete di comunicazione\), quindi le sue funzionalità e caratteristiche.



