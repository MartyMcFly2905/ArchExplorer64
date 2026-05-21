# ARCH-EXPLORER 64 ◈ Interactive Hardware Model

**ARCH-EXPLORER 64** è un'applicazione web interattiva progettata per visualizzare, navigare e comprendere l'architettura completa del calcolatore (x86-64 / PCI), basata rigorosamente sul materiale didattico e le specifiche del corso di **Calcolatori Elettronici (UNIPI)**.

🚀 **Prova l'app qui**: [archexplorer64.vercel.app](https://archexplorer64.vercel.app/)

## Funzionalità Principali
* **Diagramma Hardware Interattivo**: Navigazione intuitiva tramite clic sui blocchi (CPU, MMU, BUS, ecc.).
* **Sidebar Contestuale**: Ogni blocco apre una vista dettagliata con:
    * **Concetti Teorici**: Spiegazioni focalizzate sui punti chiave dell'esame (es. EOI, Page Fault, TLB miss).
    * **Riferimenti Grafici**: Galleria di immagini originali (schemi a blocchi, cronogrammi, flussi di dati) estratti dal materiale del corso.
* **Visual Evidence**: Rappresentazione dinamica dei segnali hardware (es. `M/IO#`, `HOLD/HLDA`, `INTA`) per chiarire le interazioni tra componenti.
* **Analisi dell'Implementazione**: Dettagli su come il nucleo didattico realizza le astrazioni (es. salvataggio contesto, gestione semafori, preparazione PRD per il DMA).

## Obiettivi Didattici
L'applicazione copre l'intero spettro del materiale d'esame, inclusi:
* **Pipeline e Out-of-Order**: Pipeline a 5 stadi, Hazard (RAW/Controllo), Branch Prediction e ROB.
* **Gestione della Memoria**: Page tables a 4 livelli, TLB, Huge Pages (2MiB/1GiB) e finestra fisica (FM).
* **Interrupt e I/O**: Protocollo INTR/INTA, configurazione APIC, polling vs interrupt-driven e DMA bus mastering.
* **Kernel Didattico**: Struttura dei processi, scheduler preemptive, primitive di sincronizzazione e gestione del contesto.

## Stack Tecnologico e Realizzazione
L'applicazione è stata sviluppata con un focus particolare sulla portabilità, le prestazioni e la semplicità di esecuzione nel browser:

* **Architettura "Zero-Build"**: L'app è progettata per essere eseguita istantaneamente. Sfrutta **React 18** insieme a **Babel in-browser** per compilare il codice JSX direttamente lato client, eliminando la necessità di configurazioni complesse o build step.
* **Visualizzazione SVG Dinamica**: L'intero schema hardware è renderizzato tramite componenti SVG reattivi.
* **Gestione Dati Centralizzata**: La conoscenza teorica e la struttura hardware sono memorizzate in un database JSON integrato. Questo approccio permette di associare dinamicamente le descrizioni teoriche ai nodi grafici, facilitando l'aggiornamento dei contenuti senza dover modificare la logica di rendering.
* **Performance e Styling**: Basata su Vanilla CSS con un approccio minimale, l'interfaccia è pensata per essere leggera e accessibile, ottimizzata per la consultazione rapida durante la preparazione dell'esame.

---

*Progetto personale non ufficiale, realizzato per supportare la preparazione all'esame di Calcolatori Elettronici (UNIPI).*
