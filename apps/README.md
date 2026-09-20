# Aplikacije

Ovde se nalaze planirani portali i korisničke aplikacije za create tok i naredne faze.

## Aktivni skelet

- `public-portal/` — javni portal za programe, javne informacije i izveštaje
- `user-portal/` — korisnički tokovi za profil, dokaze i status licence
- `partner-portal/` — partnerski tokovi za procenu, potvrdu učinka i angažmane
- `admin-portal/` — administrativni tokovi za audit, KPI i regulatorni nadzor

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/module-readiness-overview.md`, `docs/06-developer/mvp-create-implementation-plan.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Pravilo granica

- aplikacije orkestriraju korisničke tokove, ali ne dupliraju domenska pravila iz paketa i servisa
- osetljivi tokovi moraju jasno razlikovati korisnički, partnerski i interni pristup
- svaki novi interfejs mora navesti izvorni dokument, ciljnu ulogu, ownership i zavisne API ugovore
- create ownership, statusi i release kontrole vode se centralno kroz `docs/06-developer/README.md`

## Readiness i release

- `apps/` se otvara tek nakon potvrđenih `specs/api/`, `packages/` i `services/` zavisnosti
- svaki portal mora pokazati kontrolne tačke pristupa, audit posledice i manual-review signal kada je relevantno
- završna spremnost portala proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
