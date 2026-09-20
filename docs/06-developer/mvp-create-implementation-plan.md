# MVP create plan implementacije

## Cilj

Pretvoriti postojeću dokumentacionu osnovu u operativan put ka MVP implementaciji početnog create toka uz jasne domenske granice, ugovore, validaciju, ownership i kontrole usklađenosti.

## Repo-wide prioritetna komanda

- jezgro MVP create toka je profil, dokazi, procena, odluka, licenca i audit
- svi tehnički slojevi moraju pokazati kako podržavaju ovo jezgro ili ostaju van opsega prvog talasa
- nijedan sporedni modul ne dobija prioritet nad stabilizacijom create jezgra, source-of-truth-a i kontrolnih dokumenata
- shared, service, app i test slojevi otvaraju se isključivo fazno prema `docs/06-developer/README.md` i `module-readiness-overview.md`

## Šta zaključavamo odmah

- prioritetne domene za MVP
- razvojni lifecycle i pravila promene
- minimalni create tok i njegove izlaze
- mapiranje dokumentacije na buduće aplikacije, servise, pakete, API ugovore i testove
- obavezne bezbednosne, audit i regulatorne kontrole
- početni ownership i release model za create tok

## Šta ostaje otvoreno do potvrde MVP-a

- izbor programskih jezika i framework-a
- finalna granularnost servisa i infrastrukturnih komponenti
- dubina lokalnih regulatornih integracija po jurisdikcijama
- sekundarni i kasniji korisnički tokovi izvan početnog create opsega
- finalna automatizacija build i deploy sloja

## Prvi MVP create opseg

U prvi MVP ulaze samo sledeći poslovni koraci:

1. kreiranje profila
2. unos dokaza
3. osnovna procena
4. potvrda rezultata i odluke
5. izdavanje ili odbijanje licence
6. pregled statusa i istorije
7. kompletan audit zapis

## Van opsega prvog MVP-a

- napredna orkestracija više jurisdikcija po istom korisničkom toku
- sekundarni onboarding tokovi koji ne utiču na licencu
- duboke partnerske integracije bez potvrđenih ugovora
- napredna analitika iznad osnovnih KPI ulaza
- potpuno automatizovane AI odluke bez ljudske revizije

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
| Odluka i potvrda rezultata | portal partnera/admin + servis procene | odluka, rezultat, žalba | preliminarni rezultat, pravila odluke | potvrđen rezultat ili potreba za korekcijom | ručna revizija, žalbeni put, audit odluke |
| Izdavanje licence | portal partnera/admin + servis licenci | licenca, status licence | potvrđen rezultat, pravilo licence | aktivna ili odbijena licenca | regulatorna pravila, ovlašćenja, audit |
| Pregled statusa | portal korisnika + servis licenci | licenca, obnova licence | identitet korisnika | trenutni status i istorija | kontrola pristupa, konzistentnost statusa |
| Audit zapis | audit servis + admin portal | audit događaj | događaji iz svih prethodnih koraka | pregled traga i KPI ulazi | neizmenjivost, korelacija događaja |

## Minimalni deliverables

- zaključan developer indeks
- zaključan MVP create implementation plan
- ownership mapa po domenima i artefaktima
- status and events katalog
- traceability matrica
- API contract set za v1 create tok
- referentni test paketi
- release gate checklista za dokumentaciju, ugovore i implementaciju
- ADR skup za ključne tehničke odluke

## Prioritetni redosled izgradnje

1. profil i identitet
2. dokazi i validacija unosa
3. procena i odluka
4. licence i statusi
5. audit i KPI
6. regulatorna pravila
7. partneri i angažmani
8. šire integracije i dodatni tokovi tek nakon stabilizacije jezgra

## Redosled rada

1. zahtev se preuzima iz produktne ili policy dokumentacije
2. domen i granice modula se potvrđuju u razvojnom sloju
3. API ugovor i deljeni modeli se definišu pre implementacije
4. test i audit posledice se evidentiraju pre početka rada
5. implementacija se otvara tek kada je promena spremna prema `definition-of-ready.md`
6. završetak se potvrđuje prema `definition-of-done.md` i `release-gates.md`

## Pravilo faznog otvaranja implementacije

- prvi se zaključava developer/create governance sloj u `docs/06-developer/`
- zatim se potvrđuju v1 ugovori i deljeni domenski jezik u `specs/api/` i `packages/`
- tek potom se otvaraju servisne granice koje zavise od tih ugovora
- zatim se otvara aplikativni skelet koji koristi potvrđene servisne i ugovorne granice
- test slojevi se šire paralelno sa svakim novim ugovorom, servisom, aplikacijom i statusom, ne nakon završetka izvršnog rada
- partneri, dodatne integracije i širi tokovi ostaju zatvoreni dok jezgro profila, procene, licence i audita ne postane stabilno

## Obavezne kontrolne tačke

- minimizacija podataka i role-based pristup
- audit trag za profile, procene, licence i regulatorne izuzetke
- ljudska revizija za visoko-rizične AI odluke
- mogućnost žalbe i korektivne putanje
- lokalna regulatorna ograničenja kada utiču na izdavanje ili važenje licence
- veza između ugovora, statusa, testova i ownership-a

## Faze stvarne izgradnje

### Faza 1 — formalizacija developer upravljanja
- zaključati lifecycle, change-management, ready/done i release gates
- potvrditi ownership mapu i source-of-truth raspodelu
- uskladiti tehničke README skelete sa centralnim governance pravilima

### Faza 2 — zaključavanje MVP create opsega
- potvrditi jedinstveni create tok i granice prvog izdanja
- jasno razdvojiti in-scope i out-of-scope funkcionalnosti
- uskladiti traceability i readiness dokaze za prioritete jezgra

### Faza 3 — domain i status standardizacija
- zaključati entitete, statuse, događaje i prelaze
- standardizovati nazivlje kroz dokumente i buduće module
- uskladiti audit događaje, greške i manual-review signale sa poslovnim odlukama

### Faza 4 — API i shared package sloj
- pripremiti osnovne ugovore za profil, procenu, licencu, partnera i audit
- definisati zajedničke domenske modele, statuse, validacije i greške
- uvesti traceability između zahteva, modela, interfejsa i test slojeva

### Faza 5 — skelet modula
- otvoriti module u `apps/`, `services/`, `packages/`, `specs/api/` i `tests/` u faznom redosledu
- dokazati ownership, source-of-truth i release vezu za svaki sloj
- zadržati fokus na create jezgru pre širenja na sporedne tokove
