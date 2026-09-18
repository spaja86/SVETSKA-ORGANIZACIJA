# ADR-0003: Developer/create governance framework

## Status

Prihvaćeno

## Kontekst

Repozitorijum već ima dokumentacionu osnovu, razvojni indeks i početni MVP create plan. Za prelazak iz planiranja u kontrolisanu realizaciju potrebno je formalizovati jedinstveni lifecycle, definition of ready/done, release vrata, ownership mapu, katalog statusa i skelet direktorijuma koji povezuje dokumentaciju sa budućom implementacijom.

## Odluka

Usvaja se jedinstveni developer/create framework sa sledećim obaveznim pravilima:

- svaki doprinos prolazi redosled zahtev → domen → odluka → API i modeli → test posledice → audit i usklađenost → implementacija → verifikacija
- `docs/06-developer/` ostaje centralno mesto za upravljanje spremnošću, završetkom, ownership-om, release vratima i dodatnim kontrolnim planovima
- `apps/`, `services/`, `packages/`, `specs/api/` i `tests/` otvaraju se kroz neutralan skelet pre izbora konkretne tehnologije
- verzionisani API ugovori i test paketi se održavaju kao obavezna veza između dokumentacije i buduće implementacije
- audit, bezbednost, privatnost, regulatorna pravila i AI governance tretiraju se kao prvi sloj, ne kao naknadni dodatak

## Posledice

- repozitorijum dobija proverljiv put od dokumentacije do implementacije bez gubitka traga odluke
- budući implementacioni talasi moraju ažurirati ownership, traceability, release gate i test posledice kada otvaraju nove module
- tehnološke odluke ostaju otvorene dok zaseban ADR ne potvrdi konkretan arhitektonski smer
