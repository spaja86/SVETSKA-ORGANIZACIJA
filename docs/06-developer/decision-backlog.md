# Decision backlog

## Svrha

Ovde se čuvaju otvorena pitanja koja zahtevaju upravljačku potvrdu ili ADR pre punog implementacionog zaključavanja.

## Otvorene odluke visokog prioriteta

| Tema | Zašto je otvorena | Potreban izlaz | Blokira |
| --- | --- | --- | --- |
| Tehnološki stack aplikacija | želimo da izbegnemo rano zaključavanje tehnologije | ADR sa kriterijumima izbora | izvršni kod u `apps/` |
| Tehnološki stack servisa | servisne granice su poznate, ali runtime nije zaključan | ADR sa interoperabilnim smernicama | izvršni kod u `services/` |
| Format verzionisanja ugovora | postoji v1 skelet, ali bez formalne šeme kompatibilnosti | ADR ili standard ugovora | dugoročno održavanje `specs/api/` |
| Model orkestracije create toka | tok je dokumentovan, ali nije izabrana izvršna koordinacija | ADR za koordinaciju događaja i tranzicija | Faza 6 MVP toka |
| Model observability implementacije | postoje zahtevi za KPI i audit, ali ne i tehnički mehanizam | ADR ili operativni standard | produkciona spremnost |
| Regulatorna lokalizacija | globalni model postoji, ali lokalni override mehanizam nije zaključen | policy + tehnička odluka | proširenje po jurisdikcijama |

## Pravilo rada sa backlog-om

- stavka ostaje ovde dok ne dobije ADR ili upravljačku odluku
- nijedna stavka ne sme ostati skrivena u README fajlu ako blokira create tok
- zatvorene stavke se premeštaju u odgovarajući ADR ili kontrolni dokument
