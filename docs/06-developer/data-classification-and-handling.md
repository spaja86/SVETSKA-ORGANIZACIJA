# Klasifikacija i rukovanje podacima

## Svrha

Ovaj dokument uvodi minimalnu klasifikaciju podataka za identitet, dokaze, procene, licence i regulatorne artefakte.

## Kategorije podataka

| Kategorija | Primeri | Minimalne kontrole |
| --- | --- | --- |
| javni podaci | javne informacije portala, opšti programi, javni KPI rezimei | kontrola verzije i integriteta |
| interni operativni podaci | partner angažmani, status procesa, operativne napomene | role-based pristup i audit promene |
| osetljivi lični podaci | identitet korisnika, profilni podaci, istorija licence | minimizacija, ograničen pristup, retencija |
| osetljivi dokazni podaci | dokumenti, potvrde kompetencija, izvori dokaza | validacija porekla, retencija, audit pristupa |
| regulatorni podaci | lokalna pravila, izuzeci, osnov zabrane | sledljivost izvora, verzionisanje, odobren pristup |

## Pravilo rukovanja

- najmanji neophodan pristup po ulozi i koraku toka
- svaki unos dokaza mora navesti poreklo, vezu sa profilom i očekivanu retenciju
- regulatorni override mora imati razlog, ulogu i audit evidenciju
- test i ugovorni dokumenti moraju eksplicitno navesti kada koriste osetljive ili regulatorne podatke kao primer domena
