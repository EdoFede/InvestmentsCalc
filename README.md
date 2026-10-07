# Calcolatore investimento reale

Quanto vale davvero un investimento: al netto di costi e tasse, ed espresso in euro di oggi, cioè tenendo conto dell'inflazione.

È una singola pagina HTML, senza installazione né server: si apre nel browser e funziona.

**[Apri il calcolatore](https://edofede.github.io/InvestmentsCalc/Calcolo%20investimento.html)**

## Come si usa

Usa il link sopra, oppure scarica `Calcolo investimento.html` e aprilo in un browser. Serve la connessione a internet solo per caricare Chart.js e i font.

I parametri vengono ricordati dal browser tra una visita e l'altra. Il pulsante **Salva con questi parametri** scarica una copia della pagina che si riapre già con i valori attuali, utile per conservare o condividere uno scenario.

## Calcolatori

| Scheda | Domanda |
| --- | --- |
| **Accumulo** | Quanto avrò a fine piano? |
| **Obiettivo** | Quanto devo versare per arrivare a una certa cifra? |
| **Prelievo** | Quanto posso prelevare, o quanto dura il capitale? |
| **Confronto** | Quale di due piani conviene? |

### Accumulo

Proietta un piano di accumulo (PAC) con versamento iniziale e versamenti periodici.

- **Versamenti**: iniziale e periodici, con frequenza mensile, trimestrale, semestrale o annuale; possono crescere con l'inflazione e interrompersi prima della fine.
- **Costi**: TER dei fondi, imposta di bollo, commissioni per operazione con minimo e massimo, opzione PAC gratuito.
- **Tasse**: aliquota sulle plusvalenze applicata al prelievo.
- **Risultati**: valore finale, composizione, proiezione nominale e proiezione tassata e deflazionata, tabella anno per anno.
- **Scenari di mercato**: 2.000 simulazioni Monte Carlo con rendimenti variabili, data una volatilità annua.

### Obiettivo

Dato un capitale da raggiungere (netto, anche in euro di oggi), calcola il versamento mensile, il versamento iniziale o la durata necessari. Il margine di sicurezza indica in quanti scenari di mercato l'obiettivo deve essere raggiunto.

### Prelievo

Dato un capitale e la parte versata (il costo fiscale), calcola quanto dura con un certo prelievo netto, oppure il prelievo sostenibile per una durata. I prelievi possono essere adeguati all'inflazione.

### Confronto

Mette due piani affiancati con gli stessi parametri dell'Accumulo e ne confronta risultati e andamento nel tempo.

## Inflazione storica

La sezione *Inflazione storica* mostra l'inflazione annua in Italia dal 1955 al 2025, con media mobile a 5 anni e medie degli ultimi 10, 20 e 30 anni. Le medie si possono usare con un clic come inflazione del calcolo.

I dati sono in `Inflazione storica Italia.csv` (separatore `;`, percentuali con la virgola). La pagina non legge il CSV: i valori sono copiati nell'array `INFL` dentro lo script. Per aggiungere un anno vanno aggiornati entrambi.

## File

| File | Contenuto |
| --- | --- |
| `Calcolo investimento.html` | L'applicazione: HTML, CSS e JavaScript in un unico file |
| `Inflazione storica Italia.csv` | Inflazione annua in Italia, 1955–2025 |

## Avvertenza

I risultati sono stime basate su ipotesi di rendimento, inflazione e costi costanti o simulati. Non sono una previsione né una consulenza finanziaria.
