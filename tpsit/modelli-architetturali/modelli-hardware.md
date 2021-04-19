# Modelli Hardware

A seconda del tipo di gestione di flusso dati e flusso informazioni si ottengono quattro possibili combinazioni.

* **SISD**: ****presenta 1 processore \(mono core\) e un solo flusso dati. [L'architettura di Von Neumann](https://www.computerscience.gcse.guru/theory/von-neumann-architecture) era di questo tipo
* **SIMD:** presenta più processori \(mono core\) e più dati. Consente l'esecuzione di **una singola istruzione** su più flussi.
* **MISD:** presenta un processore \(multi core\) e un singolo flusso dati. Modello teorico mai implementato.
* **MIMD:** presenta un'architettura multi core. Consente l'esecuzione di più istruzioni contemporaneamente. Si suddivide in:
  * **MIMD a memoria fisica condivisa:** in una macchina multi core o multi processore la memoria centrale \(RAM\) è condivisa e quindi accessibile a tutti i core/processori consentendo la collaborazione tra questi ultimi. Questa modalità richiede l'implementazione di meccanismi per l'accesso alla memoria.
  * **MIMD a memoria fisica privata:** Non c'è comunicazione o interazione tra i processori e le aree di memoria sono fisicamente separate.
* **Cluster:** insieme di computer connessi fra loro e normalmente situati fisicamente nello stesso posto \(armadio o rack\). Offre:
  * Elevate prestazioni di calcolo e grande velocità di comunicazione fra i nodi
  * Un nodo master che si occupa di attribuire i compiti agli altri

