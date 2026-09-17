# Developer + create plan implementacije

## Cilj

Pretvoriti postojeću dokumentacionu osnovu u operativan put ka MVP implementaciji početnog create toka uz jasne domenske granice, ugovore, validaciju i kontrole usklađenosti.

## Šta zaključavamo odmah

- prioritetne domene za MVP
- razvojni lifecycle i pravila promene
- minimalni create tok i njegove izlaze
- mapiranje dokumentacije na buduće aplikacije, servise, pakete, API ugovore i testove
- obavezne bezbednosne, audit i regulatorne kontrole

## Šta ostaje otvoreno do potvrde MVP-a

- izbor programskih jezika i framework-a
- finalna granularnost servisa i infrastrukturnih komponenti
- dubina lokalnih regulatornih integracija po jurisdikcijama
- sekundarni i kasniji korisnički tokovi izvan početnog create opsega

## Prioritetna implementaciona mapa po domenima

| Domen | Buduće aplikacije | Budući servisi | Budući paketi | Budući API ugovori | Budući test fokus |
| --- | --- | --- | --- | --- | --- |
| Identitet i profil | portal korisnika, administrativni portal | servis profila i identiteta | modeli profila, statusi, validacije | profil, dokaz identiteta, istorija promena | kreiranje profila, pristup i validnost unosa |
| Procena i validacija | portal korisnika, portal partnera, administrativni portal | servis procene | modeli procene, rezultata i pravila odluke | zahtev za procenu, rezultat, ljudska revizija | procena, žalba, korektivni tok |
| Licence | portal korisnika, portal partnera | servis licenci | statusi licenci, pravila obnove | izdavanje, pregled, obnova, suspenzija | validni prelazi stanja i audit odluka |
| Partneri i angažmani | portal partnera, administrativni portal | servis partnera i angažmana | modeli partnera i angažmana | akreditacija partnera, dodela angažmana | kontrola uloga i potvrda učinka |
| Audit i KPI | administrativni portal | audit servis, reporting servis | audit događaji, KPI modeli | audit događaj, KPI pregled | integritet događaja, agregacije i trag odluke |
| Regulatorna pravila | administrativni portal | regulatorni servis | modeli jurisdikcije i pravila | pravilo, ograničenje, mapiranje jurisdikcije | blokade toka po lokalnim pravilima |

## Minimalni create tok za prvi MVP

| Korak | Odgovorni modul | Ključni entiteti | Ulazi | Izlazi | Tačke validacije |
| --- | --- | --- | --- | --- | --- |
| Kreiranje profila | aplikacija korisnika + servis profila | osoba, kompetencija | osnovni identitet, profilni podaci | aktivan profil u početnom statusu | obavezna polja, pristup, audit otvaranja |
| Unos dokaza | aplikacija korisnika + servis profila | dokaz, kompetencija | dokumenti i izjave korisnika | evidentirani dokazi za procenu | format, vlasništvo nad podacima, retencija |
| Osnovna procena | portal partnera/admin + servis procene | procena, rezultat, evaluator | profil, dokazi, kriterijumi procene | preliminarni rezultat | ljudska supervizija, trag odluke, pravičnost |
| Izdavanje licence | portal partnera/admin + servis licenci | licenca, status licence | potvrđen rezultat, pravilo licence | aktivna ili odbijena licenca | regulatorna pravila, ovlašćenja, audit |
| Pregled statusa | portal korisnika + servis licenci | licenca, obnova licence | identitet korisnika | trenutni status i istorija | kontrola pristupa, konzistentnost statusa |
| Audit zapis | audit servis + admin portal | audit događaj | događaji iz svih prethodnih koraka | pregled traga i KPI ulazi | neizmenjivost, korelacija događaja |

## Redosled rada

1. zahtev se preuzima iz produktne ili policy dokumentacije
2. domen i granice modula se potvrđuju u razvojnom sloju
3. API ugovor i deljeni modeli se definišu pre implementacije
4. test i audit posledice se evidentiraju pre početka rada
5. implementacija se otvara tek kada je promena spremna prema `definition-of-ready.md`

## Obavezne kontrolne tačke

- minimizacija podataka i role-based pristup
- audit trag za profile, procene, licence i regulatorne izuzetke
- ljudska revizija za visoko-rizične AI odluke
- mogućnost žalbe i korektivne putanje
- lokalna regulatorna ograničenja kada utiču na izdavanje ili važenje licence

## Faze stvarne izgradnje

### Faza A — formalizacija developera

- završiti razvojni indeks, governance dokumente i ADR registar
- stabilizovati pravila za tok promene, ready kriterijume i release vrata

### Faza B — zaključavanje MVP create toka

- potvrditi minimalni create tok, granice opsega i traceability matricu
- definisati vlasnike po domenima i početnim artefaktima

### Faza C — API i deljeni domen

- pripremiti osnovne ugovore za profil, procenu, licencu, partnera i audit
- definisati zajedničke domenske modele i statuse
- definisati test okvire i negativne scenarije

### Faza D — početni skelet implementacije

- otvoriti prve module u `apps/`, `services/`, `packages/`, `specs/api/` i `tests/`
- zadržati tehnologiju neutralnom dok se ne potvrdi arhitektonski smer

### Faza E — prvi krajnji tok

- realizovati create tok od profila do licence i audit zapisa
- omogućiti osnovnu KPI vidljivost i administrativni pregled
