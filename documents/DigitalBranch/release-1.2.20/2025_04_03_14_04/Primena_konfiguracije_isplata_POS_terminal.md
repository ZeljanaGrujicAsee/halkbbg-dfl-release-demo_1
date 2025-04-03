# Primena konfigurcije - isplata sa POS terminala

U konfiguraciji svaki objekat ima kind i name ili literal, kind moze da bude 'report' ili 'folder',
i sa name definisemo naziv foldera koji ce biti prikazan na frontu
Ako je kind tipa folder onda je moguce da ima i polje za 'items' to je niz koji predstavlja sadrzaj tog foldera (niz moze da sadrzi i foldere i izvestaje), svaki izvestaj ima jedistveni literal.

Nakon definisanja strukture potrebno je da definisemo i same izvestaje, to radimo preko order/reports/report-definitions konfiguracije, sadrzaj kofiguracije je niz objekata, gde svaki objekat predstavlja jedan izvestaj
Svaki izvestaj ima par onsovnih polja literal, name, parameters, gateway-endpoint i render

- name - Ime izvestaja koje se prikazuje na frontu
- literal - Jedinstveni indetifikator tog izvestaja
- parameters - Niz objekata koji definisu - parametre za izvestaj
- gateway-endpoint - Endpoint koji smo defnisali prilikom pravljenja serverless-a za taj izvestaj
- render - Dodatna podesavanja za prikaz generisanog izvestaja