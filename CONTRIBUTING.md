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

## Imenovanje

- Dokumenti koriste `kebab-case` nazive.
- Direktorijumi su grupisani numerički po oblasti radi stabilnog redosleda.
- Sadržaj se primarno piše na srpskom jeziku latiničnim pismom.
- Engleski tehnički termini, nazivi standarda, spoljne specifikacije, ustaljeni nazivi direktorijuma i kanonski nazivi platformi mogu ostati na engleskom kada to povećava jasnoću ili interoperabilnost.
- Naslovi i osnovna navigacija treba da koriste srpske ekvivalente kad god postoje i kada ne umanjuju preciznost značenja.

## Tok promene

1. Identifikacija potrebe
2. Ažuriranje odgovarajuće dokumentacije
3. Revizija uticaja na arhitekturu, podatke i usklađenost
4. Evidentiranje odluke kroz ADR ili governance dokument
5. Tek zatim implementacija koda

## Kriterijumi prihvatanja

- promena je na pravom mestu u hijerarhiji repozitorijuma
- opisuje cilj, opseg i ograničenja
- ne protivreči postojećim principima
- navodi uticaj na bezbednost, privatnost i operacije kada je relevantno
