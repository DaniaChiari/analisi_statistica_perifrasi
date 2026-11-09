# ANALISI STATISTICA SU DATI DI TESI TRIENNALE
Analisi statistica in R sui dati raccolti per la tesi triennale: ***Il mutamento dall'alto "andare a" + infinito: una perifrasi dell'italiano neostandard"***

**Autrice**: Dania Chiari

**Università**: Lettere moderne (Unibo) e Dati, metodi e modelli per le scienze linguistiche (Unibo)

## Panoramica
Per la tesi triennale ho condotto un'analisi sociolinguistica volta a individuare le caratteristiche, l'origine e la diffusione della costruzione perifrastica "andare a" + infinito, impiegata senza riferimento a un effettivo spostamento spaziale. Si tratta di una perifrasi propria del cosiddetto "italiano neostandard" (Berruto, 2012), varietà i cui tratti non godono, a differenza di quelli dell'italiano standard, dell'approvazione da parte delle grammatiche. L'italiano neostandard è sottoposto ad una duplice spinta: una proveniente dalle varietà di italiano situate nel polo basso della diastratia e della diafasia (come l’italiano popolare), da cui provengono i tratti dal “basso”, l’altra esercitata da varietà situate più in alto rispetto allo standard (come l’italiano formale aulico), da cui derivano i tratti dall’“alto”. 

La costruzione perifrastica "andare a" + infinito è annoverata tra i tratti provenienti dall'alto, ovvero i cosiddetti *mutamenti dall'alto* (Labov, 2016) o *snobismi* (Renzi, 2012) e funge da "marcatore di formalità". Questo genere di mutamenti, infatti, è prodotto in maniera consapevole da persone di classi sociali alte o medio-alte, dunque istruite, per elevare il tono della conversazione. È bene specificare che, nonostante tale traiettoria di mutamento, anche tratti come questo non sono standard, non compaiono cioè nelle grammatiche. Ad oggi, infatti, non è presente nella norma una perifrasi impiegata con valore incoativo o culminativo in cui il verbo "andare" perde il suo statuto di verbo di movimento. Riporto alcuni esempi che dimostrano come "andare" sia impiegato con valore ausiliario e non di movimento:

- *In questa zona inizia anche la differenziazione delle cellule che **andranno a costituire** i diversi tessuti* [CORIS, prosa accademica, perifrasi culminativa].
- *Vorrei qui esporle i miei punti di vista riguardo questa situazione nel modo più autentico possibile, **andando a esaminare** i vantaggi e gli svantaggi* [Univers-ITA, perifrasi incoativa].

Sono considerate, invece, forme non perifrastiche i casi in cui "andare a" + infinito preserva il significato di movimento spaziale e casi di formule lessicalizzate del tipo “andare a finire”:
- *È aspettare l'alba con gli altri al mare, **andare a fare** colazione e avere sonno per tutto il giorno successivo* [Univers-ITA-ProGior].
- *Dove sono **andati a finire** i giovani?* [CORIS, prosa accademica].

Ho dedicato l'ultimo capitolo della mia tesi triennale alla raccolta di occorrenze di tale costrutto, tratte da testi scritti riconducibili a due corpora: 

1. CORIS (1980-2000): le occorrenze sono state ricavate dalle sue sottosezioni "prosa accademica" e "stampa", selezionando come arco temporale 1980-2000;
2. Univers-ITA (2020-2021): le occorrenze sono state ricavate dall'omonimo sottocorpus "Univers-ITA", contenente testi di taglio accademico redatti da studenti, e dal sottocorpus "Univers-ITA-ProGior", contenente testi giornalistici sempre redatti da studenti. Tutti i testi del corpus Univers-ITA sono stati prodotti tra il 2020 e il 2021.

La scelta di tali corpora e di tali sottosezioni non è casuale: da un lato, desideravo verificare un'eventuale incremento nell'utilizzo della perifrasi, dall'altro, valutare le percentuali di occorrenze in due registri testuali distinti: la prosa accademica e la prosa giornalistica. Per quanto concerne la prima analisi, ho assunto CORIS come rappresentativo della generazione precedente, dal momento che ho selezionato testi redatti dal 1980 al 2000, e Univers-ITA come rappresentativo della generazione odierna, poiché contiene testi scritti da studenti universitari dal 2020 al 2021. La seconda analisi è, invece, di natura diafasica, poiché si propone di verificare in quali testi, accademici o giornalistici, la perifrasi compare con maggiore frequenza. 

Riporto qui i dati ottenuti in formato tabellare:

| Corpus | Sottosezione | Casi perifrastici | Casi non perifrastici |
| :--- | :--- | ---: | ---: |
| CORIS | Prosa accademica | 53 | 197 |
| CORIS | Stampa | 56 | 194 |
| Univers-ITA | Prosa accademica | 119 | 48 |
| Univers-ITA | Stampa | 128 | 74 |

Specifico che, per CORIS, tra le migliaia di occorrenze rinvenute attraverso il filtro di ricerca "[lemma = “andare”] [lemma = “a”] [pos = “V_GVRB”]" ne ho selezionate casualmente 250 per ciascuna sottosezione, e verificato in seguito in quante di queste compaia “andare a” + infinito perifrastico. Per quanto concerne il corpus Univers-ITA, date le dimensioni notevolmente inferiori rispetto a CORIS, ho analizzato ogni occorrenza rilevata tramite CQL "[lemma = “andare”] [lemma = “a”] [pos: “V*”]". Il numero di occorrenze non ancora sottoposte a spoglio ammonta, rispettivamente, a 167 per Univers-ITA (prosa accademica) e a 202 per Univers-ITA-ProGior (stampa).

## Metodologia
Per i limiti imposti dalla tesi triennale avevo riportato questi dati senza sottoporli ad analisi statistica, e quindi senza constatare l'eventuale presenza di una relazione significativa tra i dati. Poiché in magistrale e durante la DGfS Summer School (Bielefeld, Germania) ho acquisito competenze in statistica inferenziale (frequentista e bayesiana) e imparato a usare R e RStudio, ho deciso di condurre un'analisi statistica su questi dati. 

## Struttura
```
analisi_statistica_perifrasi/
├── data/
│   └── dati_occorrenze.csv         # Dataset con i conteggi disaggregati
├── analisi01_chi_quadrato.Rmd      # Sorgente R Markdown (codice, test e commenti)
├── analisi01_chi_quadrato.html     # Report renderizzato in HTML per il web
├── .gitignore
└── README.md
```

## Dati
### dati_occorrenze.csv
Il file in questione contiene i conteggi relativi alle occorrenze perifrastiche e non perifrastiche in ciascuna delle due sottosezioni (prosa accademica e stampa) di CORIS e Univers-ITA.

## Esecuzione e visualizzazione
Puoi consultare l'analisi formattata con i grafici a questo link:
[Visualizza Report Analisi Chi-Quadrato](https://daniachiari.github.io/analisi_statistica_perifrasi/analisi01_chi_quadrato.html)

Per eseguire l'analisi in locale clonare il repository:
git clone [https://github.com/DaniaChiari/analisi_statistica_perifrasi.git](https://github.com/DaniaChiari/analisi_statistica_perifrasi.git)
