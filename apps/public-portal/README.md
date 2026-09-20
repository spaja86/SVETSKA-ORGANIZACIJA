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
