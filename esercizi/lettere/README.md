Esercitazione in preparazione alla verifica  
Data la seguente struttura DTD creare un file XML chiamato “lettere.xml”. Successivamente, convertirlo con
linguaggio JSON all’interno di un file HTML chiamato “lettere.html”. Infine, utilizzare una funzione per
interrogare l’archivio. Fare in modo che venga visualizzato un prompt che chieda “quale lettera si vuole
vedere”, quindi inserire tre lettere, poi visualizzare un prompt che chieda “quale dettaglio visualizzare”.  
Per esempio:
- Quale lettera? 2
- Quale dettaglio? 3 (indicare nel prompt a cosa corrisponde: 1=nome_m, 2=cognome_m, ecc…)

N.B.: nella seconda domanda includere l’opzione che permetta di visualizzare tutti i dettagli

```xml
<!DOCTYPE lettere[
<!ELEMENT lettere (lettera*)>
<!ELEMENT lettera (mittente, data, destinatario, oggetto, forma_di_saluto, corpo_del_testo, saluti_finali,
firma)>
<!ELEMENT mittente (nome_m, cognome_m, indirizzo_m, cf_m, p_iva_m)>
<!ELEMENT nome_m (#PCDATA)>
<!ELEMENT cognome_m (#PCDATA)>
<!ELEMENT indirizzo_m (#PCDATA)>
<!ELEMENT cf_m (#PCDATA)>
<!ELEMENT p_iva_m (#PCDATA)>
<!ELEMENT data (giorno, mese, anno)>
<!ELEMENT giorno (#PCDATA)>
<!ELEMENT mese (#PCDATA)>
<!ELEMENT anno (#PCDATA)>
<!ELEMENT destinatario (nome_d, cognome_d, indirizzo_d, cf_d, p_iva_d)>
<!ELEMENT nome_d (#PCDATA)>
<!ELEMENT cognome_d (#PCDATA)>
<!ELEMENT indirizzo_d (#PCDATA)>
<!ELEMENT cf_d (#PCDATA)>
<!ELEMENT p_iva_d (#PCDATA)>
<!ELEMENT oggetto (#PCDATA)>
<!ELEMENT forma_di_saluto (#PCDATA)>
<!ELEMENT corpo_del_testo (paragrafo+)>
<!ELEMENT paragrafo (#PCDATA)>
<!ELEMENT saluti_finali (#PCDATA)>
<!ELEMENT firma (#PCDATA)>
<!ATTLIST firma titolo CDATA #REQUIRED>
]>
```