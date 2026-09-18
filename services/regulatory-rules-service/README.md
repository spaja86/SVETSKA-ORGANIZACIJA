# Regulatory rules service

## Svrha

Servis za lokalna pravila, blokade, izuzetke i jurisdikcijske kontrole create toka.

## Ulazi i izlazi

- ulazi: jurisdikcija, lokalno pravilo, zahtev za override, relevantan create korak
- izlazi: blokada, izuzetak, dozvoljeni nastavak ili signal za ručnu reviziju

## Granice odgovornosti

- procenjuje regulatorna pravila po koraku toka
- ne čuva glavni profil, procenu ili licencu kao izvor istine
- svaka odluka mora ostaviti audit i razlog

## Povezani artefakti

- `packages/domain-regulatory/`
- `docs/06-developer/localization-and-jurisdiction-plan.md`
- `docs/06-developer/data-classification-and-handling.md`
- `tests/integration/README.md`
