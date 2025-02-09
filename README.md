# Data_Manipulation_and_Visualization

Questo progetto Python analizza un dataset di recensioni di vini con l'obiettivo di creare un marketplace di vini, mettendo in contatto piccoli produttori locali con acquirenti di tutto il mondo. L'analisi esplorativa dei dati (EDA) è stata utilizzata per capire le caratteristiche del dataset e per proporre una strategia per l'assortimento del marketplace. Il dataset utilizzato, disponibile su Kaggle, contiene circa 130.000 recensioni di vini, con informazioni quali varietà, provenienza, vigna, prezzo e descrizione.

**Fasi principali del progetto:**

*   **Importazione delle librerie:** Sono state importate librerie come NumPy, Pandas, Scikit-learn, Matplotlib e Seaborn per l'analisi e la visualizzazione dei dati.
*   **Caricamento e analisi iniziale del dataset:** Il dataset `winemag-data-130k-v2.csv` è stato caricato utilizzando Pandas. Le dimensioni del dataset sono state verificate (129971 righe e 14 colonne). È stato anche verificato il tipo di dati e i valori non nulli per ogni colonna.
*   **Gestione dei dati mancanti:** Le colonne non necessarie per l'analisi (come 'Unnamed: 0','description','designation', 'region_2','taster_name','taster_twitter_handle','title','region_1') sono state eliminate e i valori nulli sono stati riempiti con 0. Dopo queste modifiche, il dataset aveva 129971 righe e 7 colonne. I tipi di dati sono stati verificati dopo le modifiche.
*   **Analisi statistica:** Sono state calcolate e visualizzate alcune misure statistiche come la media e la mediana per le colonne numeriche come prezzo e punteggio.
*   **Distribuzione dei dati:** La distribuzione dei dati è stata analizzata per identificare eventuali asimmetrie. I punti sono normalmente distribuiti, mentre i prezzi mostrano una simmetria a sinistra.
*   **Rilevamento degli outliers:**  Sono stati identificati graficamente i valori outliers per le colonne 'price' e 'points' utilizzando i boxplot.
*   **Matrice di correlazione:** È stata calcolata la matrice di correlazione tra le variabili 'points' e 'price', evidenziando una correlazione del 39%.
*   **Sfoltimento del dataset:** Sono stati eliminati gli outliers utilizzando il metodo di Tukey. Gli outliers sono stati eliminati sia per la colonna 'points' che per la colonna 'price'.  Inoltre, sono stati rimossi i valori nulli nella colonna 'price'. Il dataset risultante, denominato data3, è stato visualizzato.
*   **Ulteriore sfoltimento:** Le varietà di vino con meno di 100 recensioni sono state rimosse dal dataset. È stato creato un nuovo dataset denominato `data3_merge` contenente solo le varietà con 100 o più recensioni. Le dimensioni del dataset dopo queste modifiche sono state verificate.
*   **Analisi del dataset sfoltito:** Sono state verificate le informazioni e statistiche sul dataset sfoltito `data3_merge`, quali tipi di dati,  misure statistiche, e distribuzioni.  La matrice di correlazione è stata ricalcolata, mostrando una correlazione del 53% tra punti e prezzo.
*   **Analisi delle varietà:** È stata effettuata un'analisi per identificare le varietà con il prezzo più alto e più basso, e con il prezzo medio più alto e più basso. Lo stesso è stato fatto per i punteggi. È stato anche calcolato il punteggio medio e il prezzo medio per ogni nazione.
*   **Analisi delle recensioni:** Sono state identificate le nazioni, le province, le cantine e le varietà con il maggior numero di recensioni.
*    **Visualizzazione delle top e flop 10 recensioni:** Sono stati creati grafici a barre per visualizzare le top 10 e flop 10 per numero di recensioni per nazione, provincia, cantina e varietà.
*  **Visualizzazione delle top e flop 10 punteggio medio:** Sono stati creati grafici a barre per visualizzare le top 10 e flop 10 per punteggio medio per nazione, provincia, cantina e varietà.
*  **Visualizzazione delle top e flop 10 prezzo medio:** Sono stati creati grafici a barre per visualizzare le top 10 e flop 10 per prezzo medio per nazione, provincia, cantina e varietà.
*   **Analisi e selezione per marketplace:**
    *   È stato creato un grafico a dispersione per visualizzare la relazione tra punteggio medio e prezzo medio delle varietà.
    *   Le varietà sono state divise in tre fasce di prezzo e sono stati selezionati i primi 10 vini per punteggio medio per ogni fascia.
    *   Lo stesso processo è stato ripetuto per i vini italiani, selezionando i primi 5 vini per punteggio medio per ogni fascia di prezzo.

**Output:**
Il progetto fornisce una serie di analisi e visualizzazioni che possono essere utili per la creazione di un marketplace di vini. In particolare, l'analisi delle varietà, dei prezzi e dei punteggi, nonché le visualizzazioni delle top e flop per recensioni, punteggio medio e prezzo medio, forniscono una base per la selezione dei vini da includere nel marketplace.

**Note:**

*   Il codice è scritto in Python e utilizza librerie come Pandas, NumPy, Scikit-learn, Matplotlib e Seaborn.
*   Il progetto include anche grafici per visualizzare la distribuzione dei dati, gli outliers, le correlazioni e la selezione per il marketplace.
*   Il notebook contiene anche un'analisi specifica per i vini italiani.
