# Specifiche di Progetto

Questo progetto consiste nel realizzare un software per la gestione di un negozio di prodotti vegani.
Il software deve avere le seguenti funzionalità:
- Registrare nuovi prodotti, con nome, quantità, prezzo di vendita e prezzo di acquisto.
- Elencare tutti i prodotti presenti.
- Registrare le vendite effettuate.
- Mostrare i profitti lordi e netti.
- Mostrare un menu di aiuto con tutti i comandi disponibili.

Il software è testuale, quindi utilizzabile da riga di comando.

## NOTE

- Cerca di scrivere del buon codice organizzandolo le varie funzionalità in apposite funzioni.
- Prima di scrivere il codice, pensa a quali sono le migliori strutture dati da utilizzare: liste, tuple, dizionari, o combinazioni di esse come liste di dizionari.
- Il programma deve essere persistente, cioè le informazioni inserite dall'utente devono essere mantenute tra diverse esecuzioni del programma, per fare questo puoi utilizzare un file di testo scegliendo tu che tipo di codifica utilizzare per le informazioni.
- Assicurati che gli input inseriti dall'utente siano validi, ad esempio che i numeri siano effettivamente numeri, gestisci i casi non validi con eccezioni e messagi di errore.
- Durante un acquisto, verifica che i prodotti acquistati siano effettivamente presenti nel magazzino, nel caso negativo mostra all'utente un messaggio di errore.
- Durante l'aggiunta in magazzino, verifica se il prodotto da aggiungere è già presente magazzino, nel caso positivo aggiungi la quantità a quella già presente in magazzino, in questo caso non serve specificare di nuovo il prezzo di acquisto e di vendita, altrimenti registralo come un nuovo prodotto.
- Il profitto lordo è il totale delle vendite, cioè tutto ciò che i clienti hanno pagato, il profitto netto invece è pari al profitto lordo meno il costo di acquisto per i prodotti.

## ESEMPIO DI INTERAZIONE CON IL PROGRAMMA (in grassetto l'input dell'utente)
Inserisci un comando: **aiuto** <br/>
I comandi disponibili sono i seguenti: 
 - aggiungi: aggiungi un prodotto al magazzino
 - elenca: elenca i prodotto in magazzino
 - vendita: registra una vendita effettuata
 - profitti: mostra i profitti totali
 - aiuto: mostra i possibili comandi
 - chiudi: esci dal programma


Inserisci un comando: **aggiungi** <br/>
Nome del prodotto: **latte di soia** <br/>
Quantità: **20** <br/>
Prezzo di acquisto: **0.80** <br/>
Prezzo di vendita: **1.40** <br/>
AGGIUNTO: 20 X latte di soia <br/>
<br/>
Inserisci un comando: **aggiungi** <br/>
Nome del prodotto: **tofu** *<br/>
Quantità: **10** <br/>
Prezzo di acquisto: **2.20** <br/>
Prezzo di vendita: **4.19** <br/>
AGGIUNTO: 10 X tofu <br/>
<br/>
Inserisci un comando: **aggiungi** <br/>
Nome del prodotto: **seitan** <br/>
Quantità: **5** <br/>
Prezzo di acquisto: **3** <br/>
Prezzo di vendita: **5.49** <br/>
AGGIUNTO: 5 X seitan <br/>
<br/>
Inserisci un comando: **elenca** <br/>
PRODOTTO	QUANTITA'	PREZZO <br/>
latte di soia	20	€1.4 <br/>
tofu	10	€4.19 <br/>
seitan	5	€5.49 <br/>
<br/>
Inserisci un comando: **vendita** <br/>
Nome del prodotto: **latte di soia** <br/>
Quantità: 5 <br/>
Aggiungere un altro prodotto ? (si/no): **si** <br/>
Nome del prodotto: **tofu** <br/> 
Quantità: **2** <br/>
Aggiungere un altro prodotto ? (si/no): **no** <br/>
VENDITA REGISTRATA <br/>
5 X latte di soia: €1.40 <br/>
2 X tofu: €4.19 <br/>

Totale: €15.38 <br/>
<br/>
Inserisci un comando: **elenca** <br/>
PRODOTTO	QUANTITA'	PREZZO <br/>
latte di soia	15	€1.4 <br/>
tofu	8	€4.19 <br/>
seitan	5	€5.49 <br/>
<br/>
Inserisci un comando: **vendita** <br/>
Nome del prodotto: **seitan** <br/>
Quantità: **5** <br/>
Aggiungere un altro prodotto ? (si/no): **no** <br/>
VENDITA REGISTRATA <br/>
5 X seitan: €5.49 <br/>

Totale: €27.45 <br/>
<br/>
Inserisci un comando: **elenca** <br/>
PRODOTTO	QUANTITA'	PREZZO <br/>
latte di soia	15	€1.4 <br/>
tofu	8	€4.19 <br/>
<br/>
Inserisci un comando: **profitti** <br/>
Profitto: lordo=€42.83 netto=€19.43 <br/>
<br/>
Inserisci un comando: **storna** <br/>
Comando non valido <br/>
I comandi disponibili sono i seguenti: <br/>
- aggiungi: aggiungi un prodotto al magazzino <br/>
- elenca: elenca i prodotto in magazzino <br/>
- vendita: registra una vendita effettuata <br/>
- profitti: mostra i profitti totali <br/>
- aiuto: mostra i possibili comandi <br/>
- chiudi: esci dal programma <br/>

Inserisci un comando: **chiudi** <br/>
Bye bye
