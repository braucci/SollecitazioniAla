# Analisi delle sollecitazioni su una semiala

Applicazione didattica interattiva per l'analisi qualitativa e quantitativa delle principali sollecitazioni interne agenti su una **semiala**: taglio `T(x)`, momento flettente `Mf(x)` e sforzo normale `N(x)`.

Il progetto nasce come supporto visuale per il corso di **Costruzioni Aeronautiche** e consente di modificare i parametri geometrici e di carico della struttura, osservando in tempo reale lo schema strutturale e, dopo il calcolo, i relativi diagrammi delle sollecitazioni.

---

## Obiettivo didattico

L'applicazione ha lo scopo di aiutare lo studente a collegare tre livelli di lettura dello stesso problema strutturale:

1. **schema fisico della semiala**, con vincoli, carichi distribuiti, carichi concentrati e punti notevoli;
2. **modello statico equivalente**, con reazioni vincolari e condizioni di equilibrio;
3. **diagrammi interni**, cioè andamento di taglio, momento flettente e sforzo normale lungo la semiapertura.

L'idea centrale è rendere visibile il passaggio dalla configurazione del problema alle grandezze strutturali che governano il dimensionamento preliminare.

---

## Casi di studio disponibili

L'applicazione contiene tre configurazioni strutturali.

### 1. Ala controventata

Semiala con:

- cerniera alla radice;
- controvento in un punto intermedio;
- carico distribuito uniforme verso l'alto;
- componente assiale indotta dal controvento.

Il caso permette di evidenziare la presenza di uno sforzo normale non nullo nel tratto compreso tra la radice e il punto di attacco del controvento.

### 2. Ala a sbalzo con motore

Semiala incastrata alla radice, soggetta a:

- portanza distribuita;
- peso concentrato del motore;
- reazione verticale e momento d'incastro.

Il caso mostra la sovrapposizione degli effetti tra carico distribuito aerodinamico e carico concentrato dovuto al motore.

### 3. Ala rastremata con motore

Semiala a sbalzo con:

- distribuzione di portanza trapezoidale;
- carico concentrato del motore;
- variazione lineare del carico lungo la semiapertura.

Il caso è utile per rappresentare una distribuzione di carico più realistica rispetto al carico uniforme.

---

## Grandezze calcolate

Per ciascun caso vengono determinati e rappresentati:

- reazioni vincolari;
- eventuale momento d'incastro;
- andamento del taglio `T(x)`;
- andamento del momento flettente `Mf(x)`;
- andamento dello sforzo normale `N(x)`;
- valori massimi e minimi delle sollecitazioni;
- posizione dei punti significativi, come motore o controvento.

---

## Funzionalità principali

- Interfaccia web in un unico file HTML.
- Inserimento interattivo dei parametri geometrici e di carico.
- Aggiornamento dinamico dello schema strutturale.
- Calcolo dei diagrammi delle sollecitazioni.
- Visualizzazione grafica tramite Chart.js.
- Esportazione dei risultati numerici in formato CSV.
- Esportazione di una tavola riepilogativa in PNG adatta alla stampa.
- Layout responsivo, utilizzabile anche su schermi piccoli.
- Stile grafico ispirato a un terminale tecnico “Matrix-like”.

---

## Tecnologie utilizzate

Il progetto è realizzato con tecnologie web standard:

- **HTML5** per la struttura della pagina;
- **CSS3** per layout, animazioni e stile grafico;
- **JavaScript vanilla** per logica, calcolo e interazione;
- **SVG** per la rappresentazione degli schemi strutturali;
- **Canvas 2D** per l'esportazione della tavola in PNG;
- **Chart.js** per il tracciamento dei diagrammi.

Non sono richiesti framework o sistemi di build.

---

## Struttura del repository consigliata

```text
.
├── sollecitazioni.html
├── README.md
└── assets/
    └── preview.png
```

Il file `assets/preview.png` è facoltativo, ma consigliato per mostrare nel README una schermata dell'applicazione.

---

## Come usare il progetto

### Uso locale

È sufficiente aprire il file:

```text
sollecitazioni.html
```

con un browser moderno.

Poiché il progetto usa Chart.js e font caricati da CDN, è consigliata una connessione Internet attiva al primo caricamento della pagina.

### Pubblicazione con GitHub Pages

Per pubblicare l'applicazione:

1. caricare il file `sollecitazioni.html` nel repository;
2. rinominarlo eventualmente in `index.html`;
3. aprire le impostazioni del repository;
4. attivare **GitHub Pages** dal branch principale;
5. accedere all'indirizzo generato da GitHub.

Se il file viene rinominato in `index.html`, l'applicazione sarà caricata automaticamente come pagina principale del sito.

---

## Esempio di flusso d'uso

1. Selezionare uno dei tre casi strutturali.
2. Inserire i parametri richiesti.
3. Osservare l'aggiornamento dello schema.
4. Premere **Esegui calcolo**.
5. Analizzare reazioni vincolari e diagrammi.
6. Esportare i dati in CSV oppure generare una tavola PNG per appunti, relazioni o dispense.

---

## Significato delle grandezze

| Simbolo | Significato |
|---|---|
| `T(x)` | Taglio interno lungo la semiala |
| `Mf(x)` | Momento flettente lungo la semiala |
| `N(x)` | Sforzo normale lungo la semiala |
| `p` | Carico distribuito di portanza |
| `P₁`, `Pₘ` | Peso concentrato del motore |
| `R_R` | Reazione vincolare alla radice |
| `R_C` | Reazione del controvento |
| `M_R` | Momento d'incastro alla radice |
| `l` | Semiapertura |
| `l₁`, `l₂` | Lunghezze parziali della semiala |
| `θ` | Angolo del controvento |

---

## Nota sul modello

Il modello è pensato per uso didattico e per analisi preliminari.  
Le ipotesi adottate sono quelle della statica elementare delle travi:

- carichi applicati nel piano dello schema;
- comportamento strutturale idealizzato;
- vincoli rappresentati in forma semplificata;
- distribuzioni di carico assegnate analiticamente;
- assenza di effetti aeroelastici, torsionali o tridimensionali.

Il progetto non sostituisce software professionali di calcolo strutturale, ma costituisce uno strumento utile per comprendere il legame tra carichi esterni e sollecitazioni interne.

---

## Possibili sviluppi futuri

Alcune estensioni possibili:

- introduzione del momento torcente;
- confronto tra distribuzione uniforme, trapezoidale ed ellittica della portanza;
- esportazione automatica in PDF;
- salvataggio e caricamento di casi personalizzati;
- inserimento di unità di misura selezionabili;
- visualizzazione della convenzione dei segni;
- modalità chiara per stampa e proiezione in aula;
- integrazione con esempi guidati ed esercizi svolti.

---

## Autore

**Prof. Biagio Raucci**  
Costruzioni Aeronautiche

---

## Licenza

Scegliere una licenza prima della pubblicazione del repository.

Una scelta semplice e permissiva può essere la licenza **MIT**, se si desidera consentire il riuso e la modifica del codice mantenendo l'attribuzione dell'autore.
