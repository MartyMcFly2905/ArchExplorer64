# ARCH-EXPLORER 64 ◈ Interactive Hardware Model

**ARCH-EXPLORER 64** è un'applicazione web interattiva progettata per visualizzare, navigare e comprendere l'architettura completa del calcolatore (x86-64 / PCI), basata rigorosamente sul materiale didattico e le specifiche del corso di **Calcolatori Elettronici (UNIPI)**.

🚀 **Prova l'app qui**: [archexplorer64.vercel.app](https://archexplorer64.vercel.app/)

## Finalità
L'app è uno strumento di **supporto allo studio per l'esame orale**. Supera la staticità dei diagrammi tradizionali, permettendo di:
* **Esplorare la gerarchia hardware**: Collegare visivamente CPU, MMU, Cache, RAM e Bus.
* **Studiare i meccanismi critici**: Approfondire il *table-walk* dell'MMU, il funzionamento del bus mastering DMA, la gestione degli interrupt tramite APIC e il *context switch* del kernel.
* **Consultare documentazione tecnica**: Accedere a spiegazioni concise e rigorose, modellate sulle domande tipiche d'esame.

## Funzionalità Principali
* **Diagramma Hardware Interattivo**: Navigazione intuitiva tramite clic sui blocchi (CPU, MMU, BUS, ecc.).
* **Sidebar Contestuale**: Ogni blocco apre una vista dettagliata con:
    * **Concetti Teorici**: Spiegazioni focalizzate sui punti chiave dell'esame (es. EOI, Page Fault, TLB miss).
    * **Riferimenti Grafici**: Galleria di schemi e immagini originali estratti dal materiale del corso.
* **Visual Evidence**: Rappresentazione dei segnali hardware (es. `M/IO#`, `HOLD/HLDA`, `INTA`) per chiarire le interazioni tra componenti.
* **Analisi dell'Implementazione**: Dettagli su come il nucleo didattico realizza le astrazioni (es. salvataggio contesto, gestione semafori, preparazione PRD per il DMA)

## Obiettivi Didattici
L'applicazione copre gran parte del materiale d'esame, inclusi:
* **Pipeline e Out-of-Order**: Pipeline a 5 stadi, Hazard (RAW/Controllo), Branch Prediction e ROB.
* **Gestione della Memoria**: Page tables a 4 livelli, TLB, Huge Pages (2MiB/1GiB) e finestra fisica (FM).
* **Interrupt e I/O**: Protocollo INTR/INTA, configurazione APIC, polling vs interrupt-driven e DMA bus mastering.
* **Kernel Didattico**: Struttura dei processi, scheduler preemptive, primitive di sincronizzazione e gestione del contesto.

---

*Progetto didattico non ufficiale, realizzato per supportare la preparazione all'esame di Calcolatori Elettronici (UNIPI).*
