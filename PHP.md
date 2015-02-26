##PHP
####PHP: Caratteristiche delle variabili in PHP
Le variabili in php sono definite tramite il simbolo `$`, qualunque identificatore preceduto da tale simbolo è ritenuto una variabile.

Non sono necessarie dichiarazioni, una variabile è definita al momento del primo accesso e non ci sono controlli di tipo, un int può diventare una stringa e viceversa.

####PHP: Variabili e costanti in PHP

####PHP: Operatori aritmetici e logici di PHP
Gli operatori aritmetici sono quelli basilari, (+) addizione, (-) sottrazione, (*) moltiplicazione, (/) divisione e (%) modulo.

Quelli logici sono and, or, xor, nor ed i corrispondenti simboli (&&, ||, ...)(usati nelle strutture di controllo `if ... else`)
Inoltre vi sono gli operatori di bitwise (&, |, ~, >>, <<, ^)

Inoltre vi è un operatore di concatenazione stringhe, il punto `.`

####PHP: Array associativi in PHP
Gli array associativi sono strutture più simili a mappe che ad array, ad ogni elemento contenuto è assegnata una chiave (stringa) ed un indice incrementale, vi si può poi accedere tramite la chiave o tramite l'indice.

È possibile dichiararli esplicitamente con il metodo array, passandogli ogni tupla nella forma `'chiave' => 'valore'` o implicitamente, settando il valore di un elemento tramite chiave.

ES: `array( 'chiave1' => 1, 'chiave2' => 2);` o `array['chiave3'] = 3;`

####PHP: Strutture di controllo in PHP
Le strutture di controllo in PHP sono le classiche strutture di controllo che è possibile trovare in molti linguaggi di programmazione, esse sono: `if ... else` e `switch case`

####PHP: Gli array associativi $_POST e $_GET in PHP
Esistono alcuni array speciali che vengono sempre inizializzati da PHP, tra cui $\_GET e $\_POST che consentono l'accesso diretto ai valori passati allo script tramite i metodi GET e POST messi a dispozione del protocollo HTTP. 

####PHP: Definizione di funzioni in PHP
È possibile dichiarare una funzione usando la sintassi `function nome(parametri)` cui segue l'implementazione. Non è necessario specificare il tipo di ritorno.

####PHP: Funzioni anonime in PHP
Vengono dichiarate nel momento in cui devono essere utilizzate/passate come argomento. Il nome è omesso.

####PHP: Funzioni con numero variabile di argomenti in PHP
Vengono specificati degli argomenti opzionali nella firma della funzione facendo precedere il nome del parametro da `...`

Gli argomenti così passati sono conservati in un array che ha il nome del parametro specificato, nell'implementazione della funzione viene controllata l'esistenza di tale array ed utilizzato.

####PHP: Inclusione di file esterni in PHP
Vi sono due possibilità, `include` e `require`. Entrambe vengono usate per inserire all'interno del proprio script per porzioni di codice e librerie/framework.

Le dichiarazioni include e require sono identiche, tranne che in caso di errore :
+require produce un fatal error e blocca l'esecuzione dello script
+include produce un warning ma l'esecuzione continua

Per ognuna vi è la versione `_once` che controlla che il file sia incluso esattamente una volta sola.

####PHP: Gestione dei cookie in PHP
Viene creato l'array associativo $\_COOKIE che contiene tutte le tuple nome valore dei cooki attualmente settati.
È possibile settarne di nuovi tramite la funzione `setcookie(nome, valore)`, la quale permette di inserire anche parametri opzionali quali la data di scadenza ed il path. 

Per eliminare un cookie semplicemente si setta per sicurezza la sua scadenza a un ora indietro dal momento attuale  `setcookie('oreo', 'vanilla', time() - 3600);`

È possibile conservare array interi nei cookie, per farlo basta memorizzarli con nomi che rispettano la sintassi degli array, come `mioArray[uno]`. Gli elementi interni sono poi direttamente accessibili dall'array $_COOKIE.

####PHP: Gestione delle sessioni in PHP
L'HTTP è un protocollo stateless, cioè tra una richiesta e l'altra non è possibile conservare informazioni. PHP argina questo problema server-side utilizzando le sessioni.

Le variabili attualmente utilizzate vengono serializzate e salvate su disco, per poter essere riutilizzate in un altra pagina che riprende la stessa sessione.
Per definire se la sessione è la stessa viene memorizzato un cookie sul client con un valore random che viene poi letto per ripristinare tali variabili.

Chiamando la funzione `session_start()` si inizia una nuova sessione o si carica quella già salvata. 

È possibile terminare la sessione corrente invocando `session_destroy()`.

####PHP: Accesso a database in PHP (MySql)
È possibile effettuare l'accesso in maniera procedurale sfruttando le funzioni fornite dal modulo mysql (ormai deprecate) o le più nuove funzioni mysqli.
La procedura è simile per entrambe, prima ci si connette al servizio MySQL `$con = mysql_connect('host', 'nome', 'password')`, in seguito si seleziona un particolare database `mysql_select_db('dbname', $con)` e si effettuano le query necessarie `mysql_query("...")`. 

Quest'ultima funzione ha come valore di ritorno il risultato della query sotto forma di variabile resource di tipo mysql result. Per rendere questa variabile accessibile si usa la funzione `mysql_fetch_array($result)` che ritorna un array associativo contenente i valori ritornati dalla query.

di solito si usa come parametro di un ciclo `while` per scorere tutti i risultati ottenuti, es: `while($row = mysql_fetch_array($result))`

####PHP: Array multidimensionali in PHP

####PHP: Interazione con il browser in PHP
####PHP: La gestione di file in PHP
####PHP: Tipi di dati e variabili in PHP
Una variabile in PHP può contenere diversi tipi di dati, perché PHP tipizza dinamicamente le variabili.

I tipi base di dati esistenti in PHP sono:

+ boolean
+ integer
+ float
+ string

In PHP esistono anche tipi di dati composti, essi sono:

+ array (composto perché un array in PHP può contenere contemporaneamente tutti i tipi base o object)
+ object (sarebbero gli oggetti di PHP)

Inoltre esitono anche 3 tipi speciali, essi sono:

+ Resurces 
+ NULL ( il valore speciale NULL rappresenta una variable senza valore, una variabile è null se: gli viene assegnato il valore null, non gli è stato ancora assegnato un valore, è stata cancellata con la funzione `unset()`)

####PHP: Campo di visibilità delle variabili in PHP
In PHP le variabili possono essere globali, locali o super-globali.

__Le variabili Globali__ sono dichiarate fuori da qualunque funzione, sono accessibili da qualsiasi parte dello script.

__Le variabili Locali__ sono dichiarate dentro una funzione, è restano vibili solo a quella funzione.

__Le variabili Super-Globali__ sono quelle gestite da PHP ($\_SESSION, $\_SERVER, $\_POST, $\_GET, $\_REQUEST, $\_COOKIE, $\_ENV, $\_FILES, $GLOBALS).
L’ambito di validità delle variabili super-globali é totale, cioé sono valide sia all’interno che all’esterno delle funzioni. Inoltre va considerato che anche le costanti hanno un abito di validità super-globale.

####PHP: Funzioni su array e stringhe in PHP
In PHP sono definite alcune funzioni per operare su stringhe e array

####PHP: Gli array associativi $_SERVER e $_ENV in PHP
####PHP: Moduli auto-chiamanti e sticky-form in PHP
####PHP: Interagire con l'intestazione HTTP in PHP
In PHP per interaggire con il browser si usa la funzione `header` che ci permette di passare un header HTTP grezzo al client, la funzione `header` per fare ciò ci permette di passargli come parametro una stringa in cui definiamo il tipo di header HTTP da inviare.

####PHP: L'array associativo $_FILES
####PHP: Persistenza dei dati con PHP
####PHP: Conservazione dello stato con PHP
___
