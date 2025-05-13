# Simulatore Contenuti Amazon A+

Questo progetto è un simulatore frontend per la creazione e l'anteprima di contenuti Amazon A+ (precedentemente noti come Enhanced Brand Content - EBC). Permette agli utenti di selezionare diversi moduli di contenuto A+, inserire testi e immagini, e visualizzare un'anteprima live di come apparirebbero sulla pagina di un prodotto Amazon. Include anche funzionalità per esportare l'anteprima come immagine PNG o documento PDF.

## 🚀 Demo Live

Puoi provare una versione live di questo simulatore [qui](https://andreacastagna.info/amazon_scheda_prodotto/).


## ✨ Funzionalità Principali

* **Selezione Dinamica dei Moduli:** Scegli da una lista predefinita di moduli di contenuto A+ Premium.
* **Input di Contenuto Interattivo:**
    * Campi di testo con contatore di caratteri e limiti massimi.
    * Upload di immagini con anteprima istantanea.
    * Campi per testo alternativo (alt text) per le immagini.
* **Anteprima Live:** Visualizza immediatamente le modifiche apportate ai moduli nell'area di anteprima.
* **Configurazione Moduli:**
    * Imposta il numero massimo di moduli selezionabili.
* **Moduli Hotspot:**
    * Aggiungi moduli con hotspot interattivi.
    * Configura la dimensione dei marker degli hotspot.
    * Visualizza popup di testo al click sull'hotspot.
* **Esportazione:**
    * Esporta l'intera anteprima come immagine PNG.
    * Esporta l'anteprima come documento PDF (multi-pagina A4 o pagina singola lunga).
* **Design Responsivo:** L'interfaccia si adatta a diverse dimensioni di schermo.

## 🛠️ Tecnologie Utilizzate

* **HTML5:** Struttura della pagina web.
* **CSS3:** Stile e layout, inclusi Flexbox per la responsività.
* **JavaScript (Vanilla):** Logica dell'applicazione, manipolazione del DOM, gestione degli eventi e interattività.
* **[html2canvas.js](https://html2canvas.hertzen.com/):** Per catturare l'area di anteprima e convertirla in un'immagine canvas.
* **[jsPDF](https://parall.ax/products/jspdf):** Per generare documenti PDF dall'immagine canvas.

## ⚙️ Struttura del Progetto

* `index.html`: Il file principale che contiene la struttura HTML, gli stili CSS inline (<style>) e il codice JavaScript (<script>).
    * **Header:** Titolo dell'applicazione.
    * **Container Principale:**
        * **Controls Area (aside):**
            * Impostazioni Generali (es. max moduli).
            * Selezione Moduli (lista dei moduli disponibili).
            * Impostazioni Hotspot.
            * Input per i Contenuti dei Moduli Selezionati.
            * Opzioni di Esportazione (PNG, PDF).
        * **Preview Area (main):**
            * Visualizzazione live dei moduli A+ configurati.
    * **Footer:** Crediti.
* **JavaScript Logic:**
    * Definizione dei moduli A+ (hardcoded come array di oggetti).
    * Funzioni per:
        * Caricare e renderizzare la lista dei moduli selezionabili.
        * Aggiungere e rimuovere istanze di moduli.
        * Renderizzare i campi di input per ciascun modulo selezionato.
        * Gestire l'input di testo (con contatore caratteri) e l'upload di immagini (con anteprima).
        * Aggiornare l'anteprima live in base ai dati inseriti.
        * Gestire la logica degli hotspot (visualizzazione, posizionamento popup).
        * Esportare l'anteprima in PNG e PDF utilizzando `html2canvas` e `jsPDF`.

## 🚀 Come Avviare Localmente

1.  Clona il repository:
    ```bash
    git clone [https://github.com/cevaboyz/amazon_a-_content.git](https://github.com/cevaboyz/amazon_a-_content.git)
    ```
2.  Naviga nella directory del progetto:
    ```bash
    cd amazon_a-_content
    ```
3.  Apri il file `index.html` nel tuo browser web preferito.

Non è richiesta alcuna build o installazione di dipendenze complessa, in quanto tutte le librerie necessarie sono caricate tramite CDN.

## 📝 Possibili Miglioramenti

* **Salvataggio e Caricamento Stato:** Implementare la possibilità di salvare la configurazione corrente (moduli selezionati e contenuti) nel localStorage del browser o in un file JSON, per poterla ricaricare in seguito.
* **Ordinamento Moduli (Drag & Drop):** Permettere agli utenti di riordinare i moduli aggiunti nell'area di anteprima.
* **Più Opzioni di Personalizzazione per i Moduli:** Aggiungere più controlli per lo stile (es. colori, font) se rilevante per l'anteprima.
* **Validazione Avanzata:** Migliorare la validazione degli input, specialmente per URL di video o specifiche tecniche.
* **Esternalizzare CSS e JS:** Spostare il CSS e JavaScript in file separati (`style.css`, `script.js`) per una migliore organizzazione.
* **Aggiungere più Moduli:** Espandere la libreria di moduli A+ disponibili.
* **Localizzazione/Internazionalizzazione (i18n):** Supportare più lingue per l'interfaccia.
* **Test Unitari e di Integrazione:** Aggiungere test per assicurare la stabilità del codice.

## 🤝 Contributi

I contributi sono benvenuti! Se hai idee per migliorare questo simulatore, sentiti libero di aprire una issue o una pull request.

## 📄 Licenza

Questo progetto è rilasciato sotto la Licenza MIT. Vedi il file `LICENSE` per maggiori dettagli (se presente, altrimenti considera di aggiungerne uno).

## 🙏 Crediti

* Creato da Andrea Castagna + Gemini.
* Librerie utilizzate: `html2canvas`, `jsPDF`.

---
