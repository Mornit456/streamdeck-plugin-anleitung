# Anleitung für Linux, Windows und Mac

## API Monkey Plugin installieren:

   Das Plugin ist sowohl für OpenDeck, als auch im offiziellen Elgato-Store kostenlos erhältlich.
   <img width="2585" height="686" alt="b13" src="https://github.com/user-attachments/assets/0c84178f-af32-4ba7-8da0-86e97ca8fb22" />
   + [Elgato](https://marketplace.elgato.com/product/api-monkey-754d958d-1c8e-4734-bbc3-b01ab914e3bb)
   + [Github](https://github.com/ft-t/apimonkey)


## Benötigte Daten

+ CompanyId:
  
  <img width="1697" height="452" alt="b5" src="https://github.com/user-attachments/assets/f8e826fc-8c68-422e-8dab-4364c4763583" />
  
+ API Key:
   + In [API](https://api.papierlos.de/docs/index.html#auth) mit Papierloszugangsdaten anmelden:
     
     [<img width="1617" height="362" alt="2026-02-27_08-53" src="https://github.com/user-attachments/assets/33a45752-8912-4794-841d-ea030a30e34b" />](https://api.papierlos.de/docs/index.html#auth)
  
   + [Hier](https://api.papierlos.de/docs/index.html#get-/companies) zuerst auf "Try", dann auf "Curl" und Key auslesen (inklusive "Basic")
     
     [<img width="3834" height="1173" alt="2026-02-27_08-56" src="https://github.com/user-attachments/assets/e25ad103-6595-49bb-956a-14b9b516c76b" />
](https://api.papierlos.de/docs/index.html#get-/companies)


## Einrichtung


1. API Monkey auf gewünschtes Feld ziehen:
   
   <img width="2657" height="1380" alt="b1" src="https://github.com/user-attachments/assets/6eca7e30-99db-4f3f-849f-c40660821f22" />

2. Feld auswählen

3. Werte wie im Bild eintragen und speichern (siehe auch Beispiele unten):
   
   <img width="1780" height="597" alt="b10" src="https://github.com/user-attachments/assets/f3f0e8c4-532b-4220-92cd-8583cf380cc2" />
   
4. JSON Selector eintragen (Beispiele für Werte siehe unten):
   
   <img width="1277" height="608" alt="b8" src="https://github.com/user-attachments/assets/9d8ef65b-5f29-4145-ba9a-7573fc3b709b" />

5. Header ausfüllen:
   
   + 2x auf "Add Header" klicken:
     
     <img width="2152" height="876" alt="b9" src="https://github.com/user-attachments/assets/cba6b852-301a-444d-a676-24a4e9cf3373" />
     
   + Folgende Werte mit API-Key in jeweils ein Feld eintragen
     + Accept application/vnd.api+json
     + Authorization Apikey
       
     <img width="2144" height="355" alt="b11" src="https://github.com/user-attachments/assets/526b32d5-6409-40fc-a963-c0de3a19e64a" />
     
       
6. Fertig
    
   <img width="2115" height="1034" alt="b12" src="https://github.com/user-attachments/assets/db8b17a8-09d5-4279-a789-d43ca06370b9" />

7. Mit einen Rechtklick -> Edit lässt sich das Aussehen anpassen:

   <img width="847" height="496" alt="b15" src="https://github.com/user-attachments/assets/b01b85ae-0673-4513-bfd6-56aeab6a694e" />



## Beispiele für mögliche Einstellungen

   + Für Offene Dokumente ({id} durch CompanyId ersetzen):
      + Api Url: https://api.papierlos.de/company-info/{id}
      + Browser Url: https://app.papierlos.de/c/{id}/document/list-open-documents
      + Title Prefix: Offene\nDokumente
      + JSON Selector: data.type.openedDocuments
        
   + Unbearbeite Dokumente:
      + Api Url: https://api.papierlos.de/company-info/{id}
      + Browser Url: https://app.papierlos.de/c/{id}/document/list-unprocessed-documents
      + Title Prefix: Unbearbeitete\nDokumente
      + JSON Selector: data.type.unprocessedDocuments
        
   + Nicht abgerechnete Rechnungen
      + Api Url: https://api.papierlos.de/company-info/{id}
      + Browser Url: https://app.papierlos.de/c/{id}/invoices
      + Title Prefix: Nicht\nabgerechnete\nRechnungen
      + JSON Selector: data.type.notBilledInvoices

   



   







