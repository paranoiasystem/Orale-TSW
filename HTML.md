##HTML
####HTML: Il linguaggio di markup HTML
HTML è un linguaggio di markup, cioè utile a rappresentare in maniera strutturale dei contenuti.
Le versioni precedenti alla 5 erano definite come un subset dell'__SMGL__  ovvero un linguaggio di markup i cui elementi sono estendibili per consentire la creazione di altri linguaggi.

###HTML: La struttura di un documento HTML
Un documento HTML richiede la dichiarazione di un _doctype_ che fornisce al client una maniera per identificare il tipo di documento, di questo tipo:
`<!DOCTYPE html>`.

L'intera risorsa è poi racchiusa tra i tag `<html></html>`.

Le parti relative al documento stesso, che definiscono caratteristiche aggiuntive o includono altre risorse vengono inserite tra le tag `<head></head>`.

Infine il contenuto stesso viene racchiuso tra `<body></body>`.

####HTML: I meta tag di HTML
Il tag `<meta>` è utilizzato per dichiarare informazioni sul documento stesso. 

Spesso viene letto dai motori di ricerca per indicizzarne il contenuto, o ne identifica il tipo di caratteri impiegato.

Possibili valori possono essere: author, description, keywords, charset, ...

####HTML: Elementi HTML di una pagina Web

####HTML: Tag ed attributi HTML
Un tag html è costituito da un tag di apertura ed uno di chiusura se ha contenuto, solo di apertura altrimenti.

L'unico componente obbligatorio è il nome, specificato tra parentesi angolari vi sono poi degli attributi opzionali che prendono la forma `nome="valore"` e possono essere specificati nel tag di apertura.
es: `<span data-attribute="valore"></span>`

####HTML: Gestione dei caratteri speciali in HTML
Vi sono alcuni caratteri che non possono essere inseriti direttamente nel codice in quanto interferirebbero con la sua interpretazione (es: `<`).

Per inserire tali caratteri basta specificare il loro codice Unicode (o nome) preceduto da `&` e seguito da `;` 

es: &egrave; = `&egrave;`

####HTML: Dichiarazione di DOCTYPE
Associa il documento ad un Document Type Definition (DTD), che ne definisce la sinstassi, gli elementi costituenti (legali) e le regole da applicarvi.
Viene definito ad inizio pagina con il tag `<!DOCTYPE>`

####HTML: Utilizzo della direttiva DOCTYPE
Dalla versione 5 i nuovi browser ritengono implicita la dichiarazione quando incontrano un documento servito come `text/html`. Esso diviene pertanto utile solo ad attivare specifiche modalità (Standard mode se presente, quirk altrimenti) e per questioni di compatibilità.

####HTML: Utilizzo DTD Strict, Transitional e Frameset

####HTML: Liste di selezione in HTML
È possibile creare una lista di valori tra cui scegliere tramite l'uso del tag `<select>` al cui interno vanno annidate le varie opzioni tramite il tag `<option>`, il valore delle opzioni è conservato nell'attributo `value`.

Es: `<select name='lista'> <option value="numeroUno">Numero Uno</option>`

####HTML: Creazione di paragrafi in HTML
Un paragrafo è una porzione di documento racchiusa tra tag `<p>`

####HTML: Navigazione tra i contenuti delle pagine web

####HTML: Creazione di liste in HTML
È possibile definire una lista ordinata (numerata) mediante il tag `<ol>`, una non ordinata tramite il tag `<ul>`

Gli elementi della lista sono poi racchiusi nei tag `<li>`

####HTML: Creazione di tabelle in HTML
Definite utilizzando i tag `<table>`, al cui interno è possibile specificare header `<thead>`, body `<tbody>` e footer `<tfoot>`.

####HTML: Utilizzo delle delle tabelle in HTML
All'interno di ognuni parte della tabella si possono definire righe mediante i tag `<tr>` ed elementi (celle) tramite `<td>`.

####HTML: Creazione di moduli e controlli utente
È possibile creare un modulo tramite il tag `<form>` il quale accetta un attributo `action` che specifica il file da eseguire quando l'evento `submit` del form viene attivato e `method` che definisce il metodo HTTP da utilizzare per l'azione. 

Gli `input` contenuti nel form vengono quindi serializzati secondo lo shcema URI ed inviati.

####HTML: Creazione di ancore e collegamenti ipertestuali in HTML

####HTML: Creazione di moduli in HTML

####HTML: Suddividere la pagina in frame con HTML
I tag `<iframe>` consentono di incorporare una risorsa html esterna all'interno del documento.
Tuttavia essi sono deprecati e l'uso è sconsigliato a partire dalla versione 5,
possono essere sostituiti con l'elemento `object`.

####HTML: Inclusioni di immagini in HTML
Un'immagine può essere inclusa tramite l'utilizzo dell'apposito tag `<img>` che accetta l'attributo `src` il cui valore deve essere l'URL dell'immmagine.

####HTML: Mappe lato client in HTML
Tramite le mappe è possibile suddividere un'immagine in sezioni, definite dalla loro posizione e dimensione in pixel. Ad ogni regione è possibile assegnare un'ancora diversa che viene caricata al momento del click.

####HTML: Visualizzazione di immagini e creazione di mappe in HTML
Ancora?

####HTML: Inclusione di fogli di stile in HTML
È possibile includere un foglio di stile tramite il tag `<link/>` il cui attributo `href` ha come valore l'URL del file in questione.

Altri attributi disponibili sono:

`rel` che specifica la relazione con il documento, va settato su __stylesheet__

`type` che specifica il mime-type del file, di solito `text/css`

####HTML: Utilizzo di accesskey e tabindex nei moduli HTML
È possibile specificare dei tasti di scelta rapida in modo da scorrere fino all'elemento interessato alla pressione degli stessi, specificabili tramite l'attributo `acceskey`.

Inoltre è possibile scorrere ad un elemento alla pressione del tasto tab. Per definire l'ordine in cui gli elementi vengono raggiunti bisogna specificare l'attributo `tabindex` settandone il valore al numero di indice che si vuole assegnare. È possibile assegnarli automaticamente (dall'alto al basso) specificando un numero negativo o dando valore uguale a tutti i tab index.

Es: `<div tabindex=5>` se sono stati specificati 4 elementi prima del div allora questo sarà selezionato per quinto, altrimenti il valore serve solo come indice incrementale (se ci sono solo un div con tabindex=2 e uno con tabindex=5, valgono come 1 e 2 non 2 e 5).
