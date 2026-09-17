# Vodič za razvoj

## Svrha razvojnog sloja

Razvojna dokumentacija prevodi strateški i operativni okvir u buduće module, interfejse i pravila implementacije.

## Granice sistema

Softverski deo projekta obuhvata:
- profile korisnika i kompetencija
- procene i validaciju
- licence i njihove statuse
- partnere, angažmane i audit
- KPI, dashboarde i AI preporuke

Policy sloj ostaje izvan koda dok ne zahteva model, pravilo ili interfejs.

## Prioriteti za developere

1. model domena
2. granice modula
3. API ugovori
4. audit i bezbednost
5. testabilni MVP tokovi

## Operativni fokus razvojnog sloja

- `README.md` u ovom direktorijumu je tehnički ulaz za čitanje i sprovođenje razvoja
- `mvp-create-implementation-plan.md` povezuje strategiju, produkt, arhitekturu i buduću implementaciju
- `definition-of-ready.md` definiše kada zahtev može preći u specifikaciju ili kod
- `traceability-matrix.md` čuva vezu između zahteva, domena, API-ja, testova i audita
- `ownership-and-release-model.md` definiše vlasništvo, release vrata i klasifikaciju promena

## Standardi kvaliteta

- male i proverljive promene
- jasna razlika između domena, politike i infrastrukture
- bezbednosni i audit zahtevi moraju biti ugrađeni od početka
- ne uvoditi tehnologije pre potvrde arhitektonskog smera
