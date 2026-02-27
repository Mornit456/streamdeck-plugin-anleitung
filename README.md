# Anleitung für Linux, Windows und Mac

## Streamdeck Software installieren

+ Windows/Mac: https://www.elgato.com/de/de/s/downloads
+ Linux: https://github.com/nekename/OpenDeck

## API Monkey Plugin installieren:

   Das Plugin ist sowohl für OpenDeck, als auch im offiziellen Elgato-Store kostenlos erhältlich.
   <img width="2585" height="686" alt="b13" src="https://github.com/user-attachments/assets/0c84178f-af32-4ba7-8da0-86e97ca8fb22" />
   + [Elgato](https://marketplace.elgato.com/product/api-monkey-754d958d-1c8e-4734-bbc3-b01ab914e3bb)
   + [Github](https://github.com/ft-t/apimonkey)


## Benötigte Daten

+ CompanyId (Nur Zahlen) im Dashboard ablesen:
  
  <img width="1697" height="452" alt="b5" src="https://github.com/user-attachments/assets/f8e826fc-8c68-422e-8dab-4364c4763583" />
  
+ API Key:
   + In <a href="https://api.papierlos.de/docs/index.html#auth" target="_blank">API</a> mit Papierloszugangsdaten anmelden:
     
     [<img width="1617" height="362" alt="2026-02-27_08-53" src="https://github.com/user-attachments/assets/33a45752-8912-4794-841d-ea030a30e34b" />](https://api.papierlos.de/docs/index.html#auth)
  
   + Auf List Companies klicken
     
     <img width="645" height="585" alt="2026-02-27_11-13" src="https://github.com/user-attachments/assets/bf3285f4-7d89-4578-8d30-3cbeb5aa9de4" />


   +  Hier zuerst auf "Try", dann auf "Curl" und Key auslesen (inklusive "Basic" und ohne ")
     
   <img width="2886" height="436" alt="2026-02-27_11-15" src="https://github.com/user-attachments/assets/af54673a-0213-4b21-a8ae-5906a731f307" />



## Einrichtung

1. Streamdeck öffnen

2. API Monkey auf gewünschtes Feld ziehen:
   
   <img width="2657" height="1380" alt="b1" src="https://github.com/user-attachments/assets/6eca7e30-99db-4f3f-849f-c40660821f22" />

3. Werte wie im Bild eintragen und speichern (weitere Beispiele unten):
   Beispiel für offene Dokumente:
   + Request Type: GET   
   + Api Url: https://api.papierlos.de/company-info/id
   + Browser Url: https://app.papierlos.de/c/{id}/document/list-open-documents
   + Title Prefix: Offene\nDokumente
   + Intervall (Sec): 60
   + JSON Selector: data.attributes.openedDocuments
   
   <img width="1780" height="597" alt="b10" src="https://github.com/user-attachments/assets/f3f0e8c4-532b-4220-92cd-8583cf380cc2" />
   
4. JSON Selector eintragen:
   
   <img width="1277" height="608" alt="b8" src="https://github.com/user-attachments/assets/9d8ef65b-5f29-4145-ba9a-7573fc3b709b" />

5. Header ausfüllen:
   
   + 2x auf "Add Header" klicken:
     
     <img width="2152" height="876" alt="b9" src="https://github.com/user-attachments/assets/cba6b852-301a-444d-a676-24a4e9cf3373" />
     
   + Folgende Werte mit API-Key(inklusive Basic) in jeweils ein Feld eintragen
     + Accept application/vnd.api+json
     + Authorization Apikey
       
     <img width="2144" height="355" alt="b11" src="https://github.com/user-attachments/assets/526b32d5-6409-40fc-a963-c0de3a19e64a" />
     
6. Speichern
       
7. Fertig
    
   <img width="2115" height="1034" alt="b12" src="https://github.com/user-attachments/assets/db8b17a8-09d5-4279-a789-d43ca06370b9" />

8. Mit einen Rechtsklick -> Edit lässt sich das Aussehen anpassen:

   <img width="847" height="496" alt="b15" src="https://github.com/user-attachments/assets/b01b85ae-0673-4513-bfd6-56aeab6a694e" />



## Beispiele für mögliche Einstellungen

   + Für Offene Dokumente (id durch CompanyId ersetzen):
      + Request Type: GET   
      + Api Url: https://api.papierlos.de/company-info/id
      + Browser Url: https://app.papierlos.de/c/{id}/document/list-open-documents
      + Title Prefix: Offene\nDokumente
      + Intervall (Sec): 60
      + JSON Selector: data.attributes.openedDocuments
        
   + Unbearbeite Dokumente:
      + Request Type: GET 
      + Api Url: https://api.papierlos.de/company-info/id
      + Browser Url: https://app.papierlos.de/c/{id}/document/list-unprocessed-documents
      + Title Prefix: Unbearbeitete\nDokumente
      + Intervall (Sec): 60
      + JSON Selector: data.attributes.unprocessedDocuments
        
   + Nicht abgerechnete Rechnungen
      + Request Type: GET 
      + Api Url: https://api.papierlos.de/company-info/id
      + Browser Url: https://app.papierlos.de/c/{id}/invoices
      + Title Prefix: Nicht\nabgerechnete\nRechnungen
      + Intervall (Sec): 60
      + JSON Selector: data.attributes.notBilledInvoices

   



   







