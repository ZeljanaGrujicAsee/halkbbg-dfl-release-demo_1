# Naslov - Kako podesiti access control

U konfiguraciji navodimo koje role ne mogu da vide menije.
Menu item-e na left side meniju skrivamo u zavisnosti od role koristeci konfiguraciju na Admin Tool-u. U toj konfiguraciji se specificira koja rola ne moze da vidi koje menu item-e. Konfiguracija izgleda tako sto se u kljucu “role” definise koja rola je u pitanju, dok se u kljucu “disabled-menu-items" definise menu itemi koje treba sakriti agentu. Primer jedne konfiguracije, da se roli read-only sakrije pregled svih menu item-a osim Client arrangement:

![alt text](image.png)

	1. Korak 1 - pogledati kongig
    2. Korak 2 - Putanja ka konfiguraciji na Branch projektu: transaction/menu-items/privileges
    3. Korak 3 - izmena konfig..