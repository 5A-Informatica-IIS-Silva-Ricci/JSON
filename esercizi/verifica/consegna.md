Esercizio  
Data la seguente struttura DTD, creare un archivio con linguaggio JSON. Il database deve essere creato
all’interno di un file html, chiamato “articoli.html”.  
Successivamente, utilizzare una funzione per interrogare l’archivio. Fare in modo che venga visualizzato un
prompt che chieda “quale articolo si vuole vedere”, quindi inserire tre articoli, poi visualizzare un prompt
che chieda quale dettaglio visualizzare”.  
Per esempio:  
Quale articolo? 2  
Quale dettaglio? 3 (indicare nel prompt a cosa corrisponde: 3 = Intestazione, 4 = corpo, ecc…)  
N.B.: nella seconda domanda includere l’opzione che permetta di visualizzare tutti i dettagli.  

Nel caso in cui l’articolo o il dettaglio non fosse disponibile, visualizzare a video un messaggio di errore.  
Altrimenti, nel caso in cui tutto fosse tutto corretto stampare il titolo, di grandezza h1, “ARTICOLI” e le
informazioni dell’articolo richieste a grandezza h3, in questa modalità:  
Stai visualizzando le informazioni relative all’articolo 1:  
Titolo: Articolo1  
Sottotitolo: Sottotitolo1  
Ecc…  
Struttura DTD:  
```dtd
<!DOCTYPE articoli [
<!ELEMENT articoli (articolo+)>
<!ELEMENT articolo (titolo, sottotitolo, intestazione, corpo, note, autori, data)>
<!ELEMENT titolo (#PCDATA)>
<!ELEMENT sottotitolo (#PCDATA)>
<!ELEMENT intestazione (#PCDATA)>
<!ELEMENT corpo (#PCDATA)>
<!ELEMENT note (#PCDATA)>
<!ELEMENT autori (autore+)>
<!ELEMENT autore (nome, cognome, eta)>
<!ELEMENT nome (#PCDATA)>
<!ELEMENT cognome (#PCDATA)>
<!ELEMENT eta (#PCDATA)>
<!ELEMENT data (giorno, mese, anno)>
<!ELEMENT giorno (#PCDATA)>
<!ELEMENT mese (#PCDATA)>
<!ELEMENT anno (#PCDATA)>
<!ATTLIST articolo curatore CDATA #REQUIRED>
]>
```
N.B.: ci devono essere due autori per articolo