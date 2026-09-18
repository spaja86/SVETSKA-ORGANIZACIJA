# Vodič za razvoj

## Svrha razvojnog sloja

Razvojna dokumentacija prevodi strateški i operativni okvir u buduće module, interfejse, kontrole kvaliteta i pravila implementacije.

## Granice sistema

Softverski deo projekta obuhvata:
- profile korisnika i kompetencija
- dokaze, procene i validaciju
- licence i njihove statuse
- partnere, angažmane i audit
- KPI, dashboarde i AI preporuke
- regulatorna pravila koja utiču na create tok i odluke

Policy sloj ostaje izvan koda dok ne zahteva model, pravilo ili interfejs.

## Prioriteti za developere

1. model domena
2. granice modula
3. API ugovori
4. audit, bezbednost i privatnost
5. testabilni MVP create tokovi
6. kontrolisano otvaranje skeleta repozitorijuma

## Jedinstveni lifecycle

Obavezni redosled za svaki doprinos je:

1. zahtev
2. domen
3. odluka
4. API i deljeni modeli
5. test posledice
6. audit i usklađenost
7. implementacija
8. verifikacija i release odluka

Bez potvrde prethodnog koraka ne otvara se naredni korak osim kada je reč o čistoj dokumentacionoj konsolidaciji bez promene značenja.

## Operativni fokus razvojnog sloja

- `README.md` u ovom direktorijumu je tehnički ulaz za čitanje i sprovođenje razvoja
- `mvp-create-implementation-plan.md` povezuje strategiju, produkt, arhitekturu i buduću implementaciju
- `definition-of-ready.md` definiše kada zahtev može preći u specifikaciju ili kod
- `definition-of-done.md` potvrđuje da su specifikacija, skelet ili implementacija završeni
- `traceability-matrix.md` čuva vezu između zahteva, domena, API-ja, testova i audita
- `create-domain-ownership-map.md` dodeljuje odgovornost po domenima i artefaktima
- `release-gates.md` definiše kontrolne tačke za svaku klasu promene

## Standardi kvaliteta

- male i proverljive promene
- jasna razlika između domena, politike i infrastrukture
- bezbednosni, audit i regulatorni zahtevi moraju biti ugrađeni od početka
- ne uvoditi tehnologije pre potvrde arhitektonskog smera
- svaki otvoreni create korak mora imati jasan poslovni ishod i završni kriterijum
