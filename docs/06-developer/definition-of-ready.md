# Definition of Ready

Razvojni zadatak je spreman za specifikaciju, skelet ili implementaciju tek kada su ispunjeni sledeći uslovi.

## Obavezni ulazi

- postoji referenca na izvorni dokument iz `docs/01-foundation/`, `docs/02-platform/`, `docs/03-product/` ili `docs/04-policies/`
- jasno su definisani cilj, opseg, ograničenja i očekivani ishod promene
- identifikovan je domen na koji promena utiče
- određeni su vlasnik odluke, vlasnik isporuke i vlasnik kontrole
- poznato je da li promena ostaje u dokumentaciji ili otvara novi artefakt u `apps/`, `services/`, `packages/`, `specs/api/` ili `tests/`
- određen je dominantni release nivo prema `release-tier-model.md`

## Obavezna analiza

- poznat je korisnički, partnerski, administrativni ili operativni ishod koji promena podržava
- procenjen je uticaj na podatke, bezbednost, privatnost, audit i regulatornu usklađenost
- određeno je da li promena zahteva ADR, API ugovor, deljeni paket, novi servis, novu aplikaciju ili test scenarije
- definisano je šta ulazi u MVP, a šta ostaje van trenutnog opsega
- poznati su statusi, događaji i kontrolne tačke ako promena utiče na životni ciklus entiteta ili odluke
- proverene su međudomenske zavisnosti i blokatori iz `cross-domain-dependency-map.md` i `decision-backlog.md`

## Obavezni izlazi pre implementacije

- postoji trag mapiranja zahtev → domen → odluka → interfejs → validacija
- definisani su kriterijumi prihvatanja i negativni scenariji kada je promena osetljiva
- poznato je gde će sadržaj biti smešten u `apps/`, `services/`, `packages/`, `specs/api/` i `tests/` kada pređe iz dokumentacije u implementaciju
- potvrđeno je da promena ne uvodi prerano tehnološko zaključavanje bez arhitektonske odluke
- potvrđeno je da su test posledice, audit događaji i kontrole pristupa identifikovani kada su relevantni
- potvrđeno je da je dokumentaciona spremnost završena pre otvaranja tehničke realizacije ili proširenja skeleta
