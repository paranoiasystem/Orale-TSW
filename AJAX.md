##AJAX
####AJAX: L'oggetto XMLHttpRequest
Il codice Javascript, senza ricaricare la pagina, 
comunica con il server tramite l'oggetto **XMLHttpRequest**.
Tra il browser ed il server avviene uno scambio di dati
asincrono (viene comunque eseguita una richiesta HTTP.
Quindi, dopo aver creato l'oggetto **XMLHttpRequest**, può essere
eseguita una richiesta HTTP specificando lo script lato server
da invocare e la funzione JS che si occuperà di manipolare
i dati ricevuti dallo script.
L'oggetto viene creato nel seguente modo: 
```javascript
var xHttp = new XMLHttpRequest();
```
####AJAX: Utilizzo della proprietà onreadystatechange di XMLHttpRequest
**onreadystatechange** è una delle proprietà di XMLHttpRequest. Quest'ultima
contiene la funzione (callback) che processerà la risposta del server.
Quindi, se **xHttp** è un oggetto di tipo **XMLHttpRequest**, allora si usa la sintassi 
```javascript
xHttp.onreadystatechange = funzioneJs;
```
altrimenti
```javascript
xHttp.onreadystatechange = function() {
  //Il tuo codice va qui
};
```
Ovviamente **onreadystatechange** è il gestore dell'evento
**readystatechange**, scatenato ogni volta che lo stato della richiesta HTTP cambia.
Lo stato della richiesta è indicato dalla proprietà **readyState** *(0 - 4)*.
####AJAX: Utilizzo della proprietà status di XMLHttpRequest
Con la proprietà **status** indichiamo lo stato della risposta HTTP sotto forma di numero *(404 - Not Found, 200 - OK,...)*
possiamo combinare l'utilizzo della proprietà **readyState** e **status** per accertarci
che sia tutto ok con la richiesta e la risposta al server.
Esempio di utilizzo:
```javascript
xHttp.onreadystatechange = function() {
  if(xHttp.status == 200 && xHttp.readyState == 4) {
    //Adesso possiamo prelevare i dati dalla risposta del
    //server ed usarli
  }
}
```
####AJAX: Differenza di utilizzo delle proprietà responseText e responseXML
La principale differenza tra **responseText** e **responseXML** consiste nel fatto che
la prima contiene i dati trasmessi dal server sotto forma di stringa e la seconda in formato
**XML** (oggetto di tipo *documento XML*), quindi pronto per essere esaminato ed elaborato
usando gli stessi metodi per navigare all'interno del DOM HTML.
####AJAX: Modelli di applicazioni web: Classico e Ajax
@TODO
####AJAX: Il ciclo di vita di un'applicazione Ajax
@TODO
####AJAX: Il metodo open (`...`)
Il metodo **open** ha cinque argomenti, ma in genere vengono usati solo i primi tre:
- Il primo indica quale metodo HTTP usare:
  - GET
  - POST
- Il secondo indica lo script da invocare
- Il terzo, booleano, indica se la richiesta debba essere sincrona o asincrona
  - `true` - asincrona
  - `false` - sincrona

####AJAX: Il metodo send (`param`)
Il metodo **send** ha un solo parametro che si usa o no a seconda del metodo HTTP scelto:
- GET
  - Con il metodo **GET** la variabile `param` è vuota:
  ```javascript
  xHttp.send();
  ```
  altrimenti
  ```javascript
  xHttp.send(null);
  ```
  - I parametri per lo script, se necessari, devono essere indicati nella url dello
  script (`"getDati.php?nome = dario&cognome = tecchia"`) 
- POST
  - Con il metodo **POST** la variabile `param` contiene i dati da passare nella
  richiesta, i parametri sono formattati come nell'url (`"nome = dario&cognome = tecchia"`)
  ma passati al server tramite **send**.
___
