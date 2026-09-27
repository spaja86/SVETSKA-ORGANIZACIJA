# Operativni protokol za potvrdu vrha programskog ekvivalenta

## Svrha

Ovaj dokument operativno implementira obavezni redosled potvrde za inicijative koje tvrde da predstavljaju objedinjeni vrh programskog ekvivalenta u okviru „SVETSKA ORGANIZACIJA“.

## 1) Centralni okvir

- svaka inicijativa se formalno veže na `docs/06-developer/README.md` kao jedini centralni ulaz
- cilj inicijative mora biti jasno opisan kao objedinjavanje postojećeg developer/create okvira, bez uvođenja paralelnog governance sistema
- svaki zahtev koji ne može da pokaže ovu vezu vraća se na dopunu pre bilo kakvog spuštanja u niže slojeve

## 2) Source-of-truth i ownership zaključavanje

- svaka oblast mora biti mapirana na odgovarajući red u `source-of-truth-map.md`
- ownership trojke (odluka/isporuka/kontrola) potvrđuju se kroz `create-domain-ownership-map.md`
- predlog ne prolazi dalje ako ownership ili source-of-truth mapiranje ostanu implicitni ili kontradiktorni

## 3) Usklađivanje modela vrha programskog ekvivalenta

- fazni redosled otvaranja slojeva je obavezan i prati `program-equivalent-assembly-model.md`: `docs → specs/api + packages → services → apps → tests`
- meta-objedinjavanje i krovno odobrenje moraju proći kriterijume iz `montezacija-nad-montezacijama.md`
- nijedan sloj ne otvara lokalna pravila pre potvrde centralnih dokumentacionih i ugovornih zavisnosti

## 4) Zajednički jezik i kontrolni stubovi

- statusi i događaji se standardizuju isključivo kroz `domain-status-and-events-catalog.md`
- obavezni kontrolni stubovi su: bezbednost, privatnost, audit trag, manual review, regulatorne blokade i release kontrole
- lokalne varijante statusa, događaja ili kontrola nisu dozvoljene

## 5) Veza svih slojeva sa create jezgrom

- svaki artefakt mora pokazati vezu sa tokom `profil → dokazi → procena → odluka → licenca → audit`
- svaki README, ugovor i test sloj mora imati sledljivost ka source-of-truth, ownership i release pravilima
- sekundarni tokovi ostaju nižeg prioriteta dok create jezgro nema stabilne ugovore, kontrole i audit signal

## 6) Operativno upravljanje promenama

- otvorena pitanja i blokatori vode se kroz `decision-backlog.md` i odgovarajuće ADR zapise
- izuzeci se ne rešavaju lokalnim TODO beleškama u modulima
- izvršni slojevi se ne otvaraju dok readiness kriterijumi nisu potvrđeni

## 7) Gate validacija pre VRH potvrde

Svaka inicijativa mora redom proći:

1. `definition-of-ready.md`
2. `definition-of-done.md`
3. `release-gates.md`

Inicijativa se odbija ili vraća na dopunu ako:

- uvodi lokalna značenja mimo centralnog modela
- uvodi lokalne statuse ili događaje
- zaobilazi source-of-truth, ownership ili release kontrole

## 8) Mera uspeha na nivou „SVETSKA ORGANIZACIJA“

- jedan centralni developer/create okvir važi za ceo repozitorijum
- potpuna sledljivost postoji od izvornog zahteva do release odluke
- nema kontradikcija između `docs/`, `specs/api/`, `packages/`, `services/`, `apps/` i `tests/` slojeva

## Operativna primena

- ovaj protokol je obavezan za svaku inicijativu koja tvrdi da predstavlja vrh programskog ekvivalenta
- kada je inicijativa višedomenska, važe najstrože relevantne kontrole svih pogođenih domena
- svaka promena ovog protokola mora ostati usklađena sa `README.md`, `source-of-truth-map.md`, `program-equivalent-assembly-model.md` i `montezacija-nad-montezacijama.md`
