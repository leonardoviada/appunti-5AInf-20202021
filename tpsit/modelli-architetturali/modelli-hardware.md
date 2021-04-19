# Modelli Hardware

A seconda del tipo di gestione di flusso dati e flusso informazioni si ottengono quattro possibili combinazioni.

* **SISD**: ****presenta 1 processore \(mono core\) e un solo flusso dati. [L'architettura di Von Neumann](https://www.computerscience.gcse.guru/theory/von-neumann-architecture) era di questo tipo
* **SIMD:** presenta più processori \(mono core\) e più dati. Consente l'esecuzione di **una singola istruzione** su più flussi.
* **MISD:** presenta un processore \(multi core\) e un singolo flusso dati. Modello teorico mai implementato.
* **MIMD:** presenta un'architettura multi core. Consente l'esecuzione di più istruzioni contemporaneamente. Si suddivide in:
  * **MIMD a memoria fisica condivisa**
  * **MIMD a memoria fisica privata**
* **Cluster**

