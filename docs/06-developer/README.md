# Developer indeks

Ovaj direktorijum je centralna ulazna tačka za tehničko upravljanje, MVP create planiranje i pripremu repozitorijuma za kontrolisanu implementaciju.

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
21. `adrs/README.md` — arhitekturne odluke koje zaključavaju smer implementacije

## Operativni redosled rada

1. zahtev dobija referencu na izvorni dokument
2. potvrđuju se domen, opseg, ograničenja i vlasništvo
3. donosi se upravljačka ili arhitekturna odluka kada je potrebna
4. definišu se API ugovori, deljeni modeli i statusi
5. povezuju se test posledice, audit događaji i kontrole usklađenosti
6. proverava se spremnost prema `definition-of-ready.md`
7. implementacija ili proširenje skeleta počinje tek nakon potvrde spremnosti
8. završetak se potvrđuje prema `definition-of-done.md` i `release-gates.md`

## Pravilo dokumentovanja

- svaki tehnički artefakt mora imati referencu na izvorni strateški, produktni ili policy dokument
- svaki domen mora imati definisane vlasnike odluke i isporuke
- svaki interfejs mora imati vezu sa testovima, auditom i statusima kada je relevantno
- bezbednost, privatnost, audit i regulatorna usklađenost ulaze u dizajn od početka
- izbor tehnologije ostaje otvoren dok ADR ne potvrdi arhitektonski smer
