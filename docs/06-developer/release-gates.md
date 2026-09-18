# Release vrata

## Svrha

Release vrata obezbeđuju da svaka promena prođe kroz isti skup kontrola pre prelaska u narednu fazu.

## Gate 1 — dokumentaciona spremnost

- problem i cilj su jasni
- postoji referenca na izvorni dokument
- opseg i ograničenja su potvrđeni
- ownership je evidentiran
- source-of-truth za oblast je poznat

## Gate 2 — domenska i arhitekturna spremnost

- domen i granice odgovornosti su potvrđeni
- potreba za ADR-om je rešena
- statusi, događaji i prelazi stanja su identifikovani
- nema ranog tehnološkog zaključavanja bez odluke
- zavisnosti prema drugim domenima su mapirane

## Gate 3 — ugovorna spremnost

- postoji minimalni API ugovor ili odluka zašto još ne postoji
- validacije, greške i audit posledice su definisane
- veza sa paketima, servisima i aplikacijama je jasna
- test posledice su poznate
- paginacija, identifikatori i statusne tranzicije su dosledni

## Gate 4 — implementaciona spremnost

- `definition-of-ready.md` je zadovoljen
- postoji plan za kontrolu pristupa, minimizaciju podataka i retenciju
- postoji plan za audit i operativni signal
- izabrano mesto artefakta u repozitorijumu je potvrđeno
- ručna revizija je definisana za high-risk odluke kada je potrebna

## Gate 5 — završetak promene

- `definition-of-done.md` je zadovoljen
- traceability je ažuriran
- povezani README, ugovori ili skelet su usklađeni
- promene su proverene i spremne za MVP talas ili narednu fazu
- otvorene odluke su prebačene u `decision-backlog.md` ili zatvorene ADR-om

## Gate 6 — MVP izdanje

- krajnji create tok je proverljiv od zahteva do audita
- pozitivni, negativni i granični scenariji imaju dokaz validacije
- regulatorne blokade, dozvole i žalbeni putevi su dokumentovani
- observability i KPI signal su definisani za produkciono praćenje
- release tier i očekivani nivo kontrole su eksplicitno potvrđeni
