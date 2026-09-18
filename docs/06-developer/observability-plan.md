# Plan observability-ja

## Svrha

Observability plan obezbeđuje da create tok bude merljiv, auditabilan i operativno vidljiv od prvog dana.

## Obavezni signali

- audit događaji za svaku ključnu akciju i odluku
- KPI ulazi za broj otvorenih profila, aktivnih procena, izdatih licenci i blokiranih tokova
- incident signal za neuspele prelaze statusa, regulatorne blokade i neuspele korelacije audita
- signal za žalbe, ručne revizije i osetljive AI preporuke

## Minimalni operativni pregled

- administrativni pregled create toka po statusima
- pregled neuspelih validacija i blokada
- pregled audit korelacije po korisniku, licenci i jurisdikciji
- pregled KPI trendova za prvi MVP talas

## Pravilo održavanja

- svaki novi domen, status ili ugovor mora navesti operativni i audit signal kada je relevantno
- observability se ažurira zajedno sa test posledicama i release vratima
