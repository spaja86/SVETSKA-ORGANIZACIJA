# CONTRIBUTING

## Svrha

Doprinosi ovom repozitorijumu moraju da jačaju jednu od tri celine:
- strateški okvir
- operativni okvir
- tehnički okvir

## Pravila doprinosa

1. Svaka veća promena mora imati jasan razlog i očekivani rezultat.
2. Strateške promene idu kroz odgovarajući dokument u `docs/01-foundation/` ili `docs/03-product/`.
3. Tehničke promene idu kroz `docs/02-platform/`, `docs/06-developer/` i ADR zapise.
4. Pravila, bezbednost i regulatorna pitanja moraju biti usklađena sa `docs/04-policies/`.
5. Nove ideje se prvo opisuju kao predlog, zatim se usklađuju sa domenom, pa tek onda prevode u implementaciju.

## Obavezni developer/create tok promene

1. identifikacija izvornog strateškog, produktnog ili policy zahteva
2. potvrda domena, opsega, ownership-a i source-of-truth artefakta
3. odluka da li promena traži governance potvrdu ili ADR
4. ažuriranje `docs/06-developer/` artefakata pre README, contract, package, service, app ili test promena
5. evidentiranje ugovornih, test, audit, data-handling i manual-review posledica
6. potvrda prema `docs/06-developer/definition-of-ready.md`
7. tek zatim otvaranje ugovora, skeleta ili izvršnog rada
8. završna provera prema `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`

## Repo-wide tehnička pravila

- `docs/06-developer/README.md` je jedina centralna ulazna tačka za create governance
- nijedan README, ugovor ili test opis ne sme redefinisati statuse, događaje, greške, ownership ili release pravila van njihovog source-of-truth artefakta
- deljeni i višedomenski artefakti preuzimaju ownership iz pogođenih domena i strože kontrole ako se domenski zahtevi razlikuju
- svi tehnički artefakti moraju imati vezu sa traceability matricom i ownership mapom kada je relevantno

## Imenovanje

- Dokumenti koriste `kebab-case` nazive.
- Direktorijumi su grupisani numerički po oblasti radi stabilnog redosleda.
- Sadržaj se primarno piše na srpskom jeziku latiničnim pismom.
- Engleski tehnički termini, nazivi standarda, spoljne specifikacije, ustaljeni nazivi direktorijuma i kanonski nazivi platformi mogu ostati na engleskom kada to povećava jasnoću ili interoperabilnost.
- Kanonski naslovi dokumenata i platformi, kao što su `CONTRIBUTING`, `AI IQ WORLD BANK` i `LICENCE ZA CELU PLANETU ZA RAD`, mogu zadržati originalni oblik kada predstavljaju prepoznatljive standarde ili identitete.
- Naslovi i osnovna navigacija treba da koriste srpske ekvivalente kad god postoje i kada ne umanjuju preciznost značenja.

## Kriterijumi prihvatanja

- promena je na pravom mestu u hijerarhiji repozitorijuma
- opisuje cilj, opseg i ograničenja
- ne protivreči postojećim principima
- navodi uticaj na bezbednost, privatnost i operacije kada je relevantno
- pokazuje source-of-truth, ownership i traceability vezu za svaki tehnički artefakt koji uvodi ili menja
- poštuje fazno otvaranje slojeva iz `docs/06-developer/module-readiness-overview.md`
