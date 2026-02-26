1. API Monkey Plugin installieren:
   <img width="2585" height="686" alt="b13" src="https://github.com/user-attachments/assets/0c84178f-af32-4ba7-8da0-86e97ca8fb22" />
   
2. API Monkey auf gewünschtes Feld ziehen:
   <img width="2657" height="1380" alt="b1" src="https://github.com/user-attachments/assets/6eca7e30-99db-4f3f-849f-c40660821f22" />

3. Feld auswählen

4. Werte wie im Bild eintragen und speichern
   <img width="1780" height="597" alt="b10" src="https://github.com/user-attachments/assets/f3f0e8c4-532b-4220-92cd-8583cf380cc2" />
   + CompanyId:
     <img width="1697" height="452" alt="b5" src="https://github.com/user-attachments/assets/f8e826fc-8c68-422e-8dab-4364c4763583" />
     
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
        
   + Bei JSON Selector eintragen
     <img width="1277" height="608" alt="b8" src="https://github.com/user-attachments/assets/9d8ef65b-5f29-4145-ba9a-7573fc3b709b" />

6. Header hinzufügen:
   + Hier mit eigenen API-Key eintragen:
     <img width="2152" height="876" alt="b9" src="https://github.com/user-attachments/assets/cba6b852-301a-444d-a676-24a4e9cf3373" />
     <img width="2144" height="355" alt="b11" src="https://github.com/user-attachments/assets/526b32d5-6409-40fc-a963-c0de3a19e64a" />
     + Accept application/vnd.api+json
     + Authorization Apikey
       
   + Falls API-Key benötigt:
      + In API mit Papierloszugangsdaten anmelden:
        <img width="2488" height="688" alt="b4" src="https://github.com/user-attachments/assets/17ff0f5f-208d-4a4c-8868-e00e28585c70" />
      + Aus api.papierlos (auf CURL drücken):
        <img width="2153" height="1363" alt="b3" src="https://github.com/user-attachments/assets/8bb739dc-fdd2-41cd-a640-9cedc6717e3c" />
     
7. Fertig
   <img width="2115" height="1034" alt="b12" src="https://github.com/user-attachments/assets/db8b17a8-09d5-4279-a789-d43ca06370b9" />



   







