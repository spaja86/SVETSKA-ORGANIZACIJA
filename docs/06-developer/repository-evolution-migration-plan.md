# Plan evolucije repozitorijuma

## Svrha

Ovaj plan vodi prelaz iz dokumentacionog repozitorijuma u aktivni product-engineering repozitorijum bez gubitka traga odluke.

## Faza 1 — dokumentaciona osnova

- konsolidacija developer sloja
- potvrda MVP create opsega
- stabilizacija ownership-a, ready/done pravila i release gate modela

## Faza 2 — ugovori i deljeni domen

- otvaranje verzionisanih API ugovora
- otvaranje deljenih domenskih paketa i kataloga statusa
- povezivanje test paketa sa traceability matricom

## Faza 3 — skelet implementacije

- otvaranje aplikativnih, servisnih i paketnih direktorijuma po potvrđenim granicama
- održavanje tehnologije neutralnom dok ADR ne potvrdi smer
- evidentiranje svih novih granica kroz README i ownership mapu

## Faza 4 — prvi end-to-end tok

- realizacija create toka od profila do licence
- uvođenje osnovnog observability i audit signala
- potvrda minimalnog administrativnog pregleda i regulatornih blokada

## Faza 5 — kontrolisano proširenje

- sekundarni tokovi, lokalizacija, spoljne integracije i dodatni KPI sloj
- dalje razdvajanje servisa samo kada granice postanu stabilne i opravdane
