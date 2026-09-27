# Public portal

## Svrha

Javni ulazni portal za programe, javne informacije, osnovni onboarding i transparentne izlaze projekta.

## Izvorni dokumenti

- `../../docs/01-foundation/mission-and-principles.md`
- `../../docs/03-product/use-cases-and-user-journeys.md`
- `../../docs/06-developer/mvp-create-implementation-plan.md`

## Minimalni opseg

- javni pregled programa i svrhe platforme
- ulazna navigacija ka korisničkom create toku
- javne smernice za profile, licence i osnovne kriterijume
- javni KPI ili statusni rezimei kada budu odobreni

## Minimalni ekrani i izlazi

- početna stranica sa objašnjenjem create toka
- pregled programa, licenci i osnovnih uslova
- navigacija ka registraciji ili kreiranju profila
- javna obaveštenja o statusu programa i pravilima

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/mvp-create-implementation-plan.md`, `../../docs/06-developer/create-domain-ownership-map.md`, `../../docs/06-developer/traceability-matrix.md`
- ownership: `../../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../../docs/06-developer/traceability-matrix.md`

## Repo-wide radni takt

- obavezni redosled ostaje: zahtev → domen → odluka → ugovor i deljeni modeli → test posledice → audit i usklađenost → implementacija → verifikacija i release odluka
- ovaj artefakt se ne otvara ako prethodni koraci nisu potvrđeni kroz `../../docs/06-developer/README.md`, `../../docs/06-developer/definition-of-ready.md` i `../../docs/06-developer/release-gates.md`
- otvorena pitanja, izuzeci i tehnološke odluke vode se kroz `../../docs/06-developer/decision-backlog.md` i `../../docs/06-developer/adrs/README.md`, ne lokalno

## Kontrolni stubovi

- bezbednost, privatnost i role-based pristup ulaze u dizajn od početka
- audit trag, manual-review signal, regulatorna blokada i korektivni tok moraju biti vidljivi kada su relevantni
- create jezgro `profil → dokazi → procena → odluka → licenca → audit` ima prioritet nad sekundarnim tokovima
- traceability od izvornog zahteva do ugovora, testova i release odluke ostaje obavezna

## Ownership i kontrola

- vlasnik odluke: produkt + tehnički vlasnici domena koje portal izlaže
- vlasnik isporuke: tehnički vlasnik implementacije portala
- vlasnik kontrole: najstroži relevantni vlasnik kontrole iz povezanih create domena
- traceability signal: portal ne uvodi samostalni domen; nasleđuje ownership i kontrolne zahteve iz create domena koje javno prikazuje

## Granice

- ne obrađuje osetljive lične podatke
- ne sadrži internu procenu niti administrativne kontrole
- ne redefiniše domenska pravila iz `../../packages/` i `../../services/`

## Readiness i release

- portal se otvara tek nakon potvrđenih ugovora, shared paketa i zavisnih servisa
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
