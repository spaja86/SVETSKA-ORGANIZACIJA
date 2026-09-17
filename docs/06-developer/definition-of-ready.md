# Definition of Ready

Razvojni zadatak je spreman za specifikaciju ili implementaciju tek kada su ispunjeni sledeći uslovi.

## Obavezni ulazi

- postoji referenca na izvorni dokument iz `docs/01-foundation/`, `docs/02-platform/`, `docs/03-product/` ili `docs/04-policies/`
- jasno su definisani cilj, opseg i ograničenja promene
- identifikovan je domen na koji promena utiče
- određeni su vlasnik odluke i vlasnik isporuke

## Obavezna analiza

- poznat je korisnički ili operativni ishod koji promena podržava
- procenjen je uticaj na podatke, bezbednost, privatnost, audit i regulatornu usklađenost
- određeno je da li promena zahteva ADR, API ugovor, deljeni paket, novi servis ili test scenarije
- definisano je šta ulazi u MVP, a šta ostaje van trenutnog opsega

## Obavezni izlazi pre implementacije

- postoji trag mapiranja zahtev → domen → interfejs → validacija
- definisani su kriterijumi prihvatanja i negativni scenariji kada je promena osetljiva
- poznato je gde će sadržaj biti smešten u `apps/`, `services/`, `packages/`, `specs/api/` i `tests/` kada pređe iz dokumentacije u implementaciju
- potvrđeno je da promena ne uvodi prerano tehnološko zaključavanje bez arhitektonske odluke
