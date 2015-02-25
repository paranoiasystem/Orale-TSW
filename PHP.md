##PHP
####PHP: Caratteristiche delle variabili in PHP
Le variabili in php sono definite tramite il simbolo `$`, qualunque identificatore preceduto da tale simbolo è ritenuto una variabile.

Non sono necessarie dichiarazioni, una variabile è definita al momento del primo accesso e non ci sono controlli di tipo, un int può diventare una stringa e viceversa.

####PHP: Variabili e costanti in PHP

####PHP: Operatori aritmetici e logici di PHP
Gli operatori aritmetici sono quelli basilari, (+) addizione, (-) sotrtrazione, * (moltiplicazione), / (divisione) e % (modulo).
Quelli logici sono and, or, xor, nor ed i corrispondenti simboli (&&, ||, ...)

Inoltre vi è un operatore di concatenazione stringhe, il punto `.`

####PHP: Array associativi in PHP
Gli array associativi sono strutture più simili a mappe che ad array, ad ogni elemento contenuto è assegnata una chiave (stringa) ed un indice incrementale, vi si può poi accedere tramite la chiave o tramite l'indice.

È possibile dichiararli esplicitamente con il metodo array, passandogli ogni tupla nella forma `'chiave' => 'valore'` o implicitamente, settando il valore di un elemento tramite chiave.

ES: `array( 'chiave1' => 1, 'chiave2' => 2); array['chiave3'] = 3;`

####PHP: Strutture di controllo in PHP

####PHP: Gli array associativi $_POST e $_GET in PHP
Esistono alcuni array speciali che vengono sempre inizializzati da PHP, tra cui $\_GET e $\_POST che consentono l'accesso diretto ai valori passati allo script tramite URI. 

####PHP: Definizione di funzioni in PHP
È possibile dichiarare una funzione usando la sintassi `function nome(parametri)` cui segue l'implementazione. Non è necessario specificare il tipo di ritorno.

####PHP: Funzioni anonime in PHP
Vengono dichiarate nel momento in cui devono essere utilizzate/passate come argomento. Il nome è omesso.

####PHP: Funzioni con numero variabile di argomenti in PHP
Vengono specificati degli argomenti opzionali nella firma della funzione facendo precedere il nome del parametro da `...`

Gli argomenti così passati sono conservati in un array che ha il nome del parametro specificato, nell'implementazione della funzione viene controllata l'esistenza di tale array ed utilizzato.

####PHP: Inclusione di file esterni in PHP
Vi sono due possibilità, `include` e `require`. La prima è utilizzata per includere risorse esterne, la seconda per porzioni di codice e librerie.
Per ognuna vi è la versione `_once` che controlla che il file sia incluso esattamente una volta sola.

####PHP: Gestione dei cookie in PHP
Viene creato l'array associativo $\_COOKIE che contiene tutte le tuple nome valore dei cooki attualmente settati.
È possibile settarne di nuovi tramite la funzione `setcookie(nome, valore)`, la quale permette di inserire anche parametri opzionali quali la data di scadenza ed il path. Per eliminare un cookie semplicemente si setta la sua scadenza a zero `setcookie('oreo', 'vanilla', 0);`

È possibile conservare array interi nei cookie, per farlo basta memorizzarli con nomi che rispettano la sintassi degli array, come `mioArray[uno]`. Gli elementi interni sono poi direttamente accessibili dall'array $_COOKIE.

####PHP: Gestione delle sessioni in PHP
L'HTTP è un protocollo stateless, cioè tra una richiesta e l'altra non è possibile conservare informazioni. PHP argina questo problema server-side utilizzando le sessioni.

Le variabili attualmente utilizzate vengono serializzate e salvate su disco, per poter essere riutilizzate in un altra pagina che riprende la stessa sessione.
Per definire se la sessione è la stessa viene memorizzato un cookie sul client con un valore random che viene poi letto per ripristinare tali variabili.

Chiamando la funzione `session_start()` si inizia una nuova sessione o si carica quella già salvata. 

È possibile terminare la sessione corrente invocando `session_destroy()`.

####PHP: Accesso a database in PHP (MySql)
È possibile effettuare l'accesso in maniera procedurale sfruttando le funzioni fornite dal modulo mysql (ormai deprecate) o le più nuove funzioni mysqli.
La procedura è simile per entrambe, prima ci si connette al servizio MySQL `mysql_connect('host', 'nome', 'password')`, in seguito si seleziona un particolare database `mysql_select_db('dbname')` e si effettuano le query necessarie `mysql_query("...")`. 

Quest'ultima funzione ha come valore di ritorno il risultato della query, che comprende tutte le righe corrispondenti alla query. Per accedere alle singole righe, contenenti quindi i valori (colonne) associati ad un'unica entrata bisogna utilizzare `mysql_fetch_row($result)` che ritorna un array contenente i valori di quella riga.

####PHP: Array multidimensionali in PHP

####PHP: Interazione con il browser in PHP
####PHP: La gestione di file in PHP
####PHP: Tipi di dati e variabili in PHP
####PHP: Campo di visibilità delle variabili in PHP
####PHP: Funzioni su array e stringhe in PHP
####PHP: Gli array associativi $_SERVER e $_ENV in PHP
####PHP: Moduli auto-chiamanti e sticky-form in PHP
####PHP: Interagire con l'intestazione HTTP in PHP
####PHP: L'array associativo $_FILES
####PHP: Persistenza dei dati con PHP
####PHP: Conservazione dello stato con PHP
___