# Developer indeks

Ovaj direktorijum je centralna ulazna tačka za tehničko upravljanje, MVP create planiranje i pripremu repozitorijuma za kontrolisanu implementaciju.

## Šta je zaključano

- jedinstveni lifecycle od zahteva do release odluke
- MVP create tok od profila do licence i audita
- početne servisne granice, deljeni paketi i test slojevi
- obavezne bezbednosne, audit i regulatorne kontrole
- centralni developer indeks kao ulaz za sve create tehničke artefakte

## Šta ostaje otvoreno

- izbor programskih jezika, framework-a i infrastrukturnih proizvoda
- finalna granularnost modula kada stvarni ugovori pokažu potrebu za podelom
- dubina lokalnih regulatornih integracija po jurisdikcijama
- tempo uvođenja AI preporuka van ručno revidiranih odluka

## Šta čeka ADR

- tehnološki stack za aplikacije, servise i pakete
- mehanizam verzionisanja ugovora i migracija kada uvedemo izvršni kod
- način orkestracije između create koraka i audit korelacije
- minimalna observability arhitektura za prvi operativni talas

## Centralni komandni sloj

- `docs/06-developer/` je jedino mesto iz kog se otvaraju create governance, ownership, kontrole i odluka da ugovorni ili implementacioni rad može da počne
- `apps/`, `services/`, `packages/`, `specs/api/` i `tests/` ne uvode novo značenje bez prethodnog zaključavanja u ovom direktorijumu
- svaka promena prvo proverava source-of-truth, ownership, release nivo i međudomenske zavisnosti pre nego što dodirne skelet ili izvršni kod
- otvorena pitanja se vode kroz `decision-backlog.md`, a ne kroz rasute TODO napomene

## Redosled čitanja

1. `developer-guide.md` — svrha razvojnog sloja, prioriteti i jedinstveni lifecycle
2. `repository-structure.md` — pravila rasporeda sadržaja i ciljni skelet repozitorijuma
3. `change-management.md` — tok promene od predloga do release odluke
4. `definition-of-ready.md` — uslovi za ulazak zahteva u specifikaciju ili implementaciju
5. `definition-of-done.md` — uslovi da specifikacija ili implementacija bude završena
6. `ownership-and-release-model.md` — bazni model vlasništva i tipovi promena
7. `create-domain-ownership-map.md` — vlasnici po domenima, artefaktima i servisnim granicama
8. `release-gates.md` — kontrolne tačke za dokumentaciju, ugovore, kod i MVP izdanje
9. `mvp-create-implementation-plan.md` — objedinjeni plan za prvi create tok
10. `domain-status-and-events-catalog.md` — standardni statusi, događaji i prelazi stanja
11. `traceability-matrix.md` — veza između dokumentacije, domena, API-ja, testova i audita
12. `create-flow-risk-matrix.md` — ključni rizici create toka i kontrolne mere
13. `role-permission-model.md` — minimalni model dozvola po ulozi
14. `observability-plan.md` — audit, KPI, incident i operativni signal
15. `repository-evolution-migration-plan.md` — prelaz iz dokumentacionog u product-engineering repozitorijum
16. `external-integration-map.md` — buduće spoljne integracije i njihove granice
17. `localization-and-jurisdiction-plan.md` — plan lokalizacije i jurisdikcijskih pravila
18. `create-data-governance-plan.md` — upravljanje podacima za create tok
19. `ai-governance-plan.md` — granice i kontrole AI preporuka i odluka
20. `reference-test-packages.md` — referentni test paketi za dugoročnu validaciju
21. `source-of-truth-map.md` — pregled koji dokument zaključava koju oblast
22. `decision-backlog.md` — otvorena pitanja i odluke koje traže ADR ili governance potvrdu
23. `module-readiness-overview.md` — spremnost slojeva `apps/`, `services/`, `packages/`, `specs/api/` i `tests/`
24. `cross-domain-dependency-map.md` — zavisnosti između create domena i kontrolnih slojeva
25. `event-naming-standard.md` — standard za imenovanje audit i domain događaja
26. `error-taxonomy.md` — standard za greške, kodove i posledice po ugovore
27. `data-classification-and-handling.md` — klasifikacija podataka i pravila rukovanja
28. `manual-review-checkpoints.md` — ručna revizija za high-risk odluke i izuzetke
29. `create-glossary.md` — jedinstven rečnik pojmova create domena
30. `release-tier-model.md` — tipovi promena i potrebni nivoi kontrole
31. `adrs/README.md` — arhitekturne odluke koje zaključavaju smer implementacije

## Ključni kontrolni artefakti pre punog build talasa

- `decision-backlog.md` — obavezno mesto za otvorena governance i ADR pitanja
- `cross-domain-dependency-map.md` — obavezna kontrola promena koje seku više domena
- `localization-and-jurisdiction-plan.md` — obavezni okvir za širenje na više regulatornih okruženja
- `observability-plan.md` — obavezni audit, KPI i operativni signal za MVP jezgro

## Operativni redosled rada

1. zahtev dobija referencu na izvorni dokument
2. potvrđuju se domen, opseg, ograničenja i vlasništvo
3. donosi se upravljačka ili arhitekturna odluka kada je potrebna
4. definišu se API ugovori, deljeni modeli i statusi
5. povezuju se test posledice, audit događaji i kontrole usklađenosti
6. proverava se spremnost prema `definition-of-ready.md`
7. implementacija ili proširenje skeleta počinje tek nakon potvrde spremnosti
8. završetak se potvrđuje prema `definition-of-done.md` i `release-gates.md`

## Pravilo otvaranja slojeva

1. `docs/06-developer/` zaključava governance, ownership, source-of-truth, statusni jezik, release kontrole i otvorene odluke
2. `specs/api/` i `packages/` otvaraju se tek kada su potvrđeni domen, ownership, statusi, greške, audit posledice i stabilan deljeni jezik
3. `services/` se otvaraju tek kada su granice odgovornosti, zabrane preklapanja i regulatorne kontrole dokumentovane
4. `apps/` se otvaraju tek kada su potvrđene uloge, ključni tokovi i zavisni ugovori
5. `tests/` se proširuju zajedno sa ugovorima, statusima, događajima i audit signalima, ne naknadno

## Prioritet zaključavanja pre implementacionog talasa

1. lifecycle, readiness, done i release gates
2. source-of-truth raspodela i ownership po domenima
3. MVP create opseg i fazni redosled otvaranja
4. statusi, događaji, greške i ručne revizije
5. v1 API ugovori i traceability veza
6. readiness dokaz za svaki sloj repozitorijuma

## Obavezni deliverables pre punog build talasa

- ažuran developer indeks i povezani governance dokumenti
- potvrđena ownership mapa i source-of-truth raspodela
- zaključan MVP create plan i traceability matrica
- v1 ugovori za profil, dokaze, procenu, licencu, partnera i audit
- README skeleti za aplikacije, servise, pakete i test slojeve
- katalog statusa, događaja, grešaka i ručnih revizija
- ažuran `decision-backlog.md` za sva otvorena governance i ADR pitanja
- potvrđena klasifikacija release nivoa za svaku veću promenu
- ažuran `cross-domain-dependency-map.md`
- ažuran `localization-and-jurisdiction-plan.md`
- ažuran `observability-plan.md`

## Pravilo dokumentovanja

- svaki tehnički artefakt mora imati referencu na izvorni strateški, produktni ili policy dokument
- svaki domen mora imati definisane vlasnike odluke, isporuke i kontrole
- svaki interfejs mora imati vezu sa testovima, auditom i statusima kada je relevantno
- bezbednost, privatnost, audit i regulatorna usklađenost ulaze u dizajn od početka
- izbor tehnologije ostaje otvoren dok ADR ne potvrdi arhitektonski smer
- promena ne otvara izvršni sloj ako `source-of-truth-map.md`, `traceability-matrix.md` i `module-readiness-overview.md` nisu usklađeni
