##HTTP
####HTTP: Il protocollo HTTP
L' **H**yper**T**ext **T**ransfer **P**rotocol è il principale sistema per la trasmissione d'informazioni sul web.

Le specifiche del protocollo sono gestite dal _World Wide Web Consortium_ (__W3C__). 

Un server HTTP generalmente resta in ascolto delle richieste dei client sulla porta 80 usando il protocollo TCP a livello di trasporto.

####HTTP: Formato dei messaggi request e response di HTTP
Una volta stabilita la connessione, il client richiede una risorsa al web server (__request__) ed il server risponde inviando o la risorsa accompagnata da un messaggio di successo o errore (__response__).

####HTTP: I metodi GET, POST, HEAD e PUT di HTTP
Metodi di lettura: GET e HEAD. Di scrittura: POST e PUT.

Metodo __Sicuro__: non altera lo stato della risorsa.

Metodo __Idempotente__: l’effetto di più richieste identiche è lo stesso di quello di una sola richiesta.

__GET__ (uno dei più utilizzati) è sicuro ed idempotente. Viene usato per richiedere dati o risorse.

__HEAD__ è una variante di GET utilizzato per avere informazioni sulla risorsa o sul server, non viene restituita tutta la risorsa ma solo i metadati associati alla risorsa richiesta (_header_).

__POST__ permette di trasmettere delle informazioni dal client al server. Non è sicuro né idempotente. Usato solitamente per sottomettere i dati di un form.

__PUT__ creando o sostituendo la risorsa specificata. PUT è idempotente ma non sicuro. 

####HTTP: Il Web ed il W3C
W3C significa “_World Wide Web Consortium_”, è un consorzio di aziende del settore informatico che si occupa di stabilire gli standard di riferimento per il Web.

####HTTP: Architettura client-server del web
L'HTTP funziona su un meccanismo richiesta/risposta (client/server):

Il __client__ è la parte che accede ai servizi o alle risorse, effettua una richiesta.

Il __server__ è comunemente un computer dedicato all'ascolto e risposta alle varie richieste

___