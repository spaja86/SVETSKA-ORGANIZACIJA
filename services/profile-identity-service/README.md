# Profile identity service

## Svrha

Servis za profil, identitet i dokaze kao ulazni sloj create toka.

## Ulazi i izlazi

- ulazi: profilni podaci, identitet, dokazi, korekcije korisnika
- izlazi: status profila, evidencija dokaza, događaji profila i validacioni ishodi

## Granice odgovornosti

- upravlja profilom, identitetom i dokazima
- ne donosi konačnu odluku procene ili licence
- ne redefiniše zajedničke modele van `../../packages/domain-profile/`

## Povezani artefakti

- `../../specs/api/v1/profile-contract.md`
- `../../specs/api/v1/evidence-contract.md`
- `../../packages/domain-profile/`
- `../../packages/shared-validation/`
- `../../tests/domain/README.md`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/domain-status-and-events-catalog.md`, `../../docs/06-developer/data-classification-and-handling.md`, `../../docs/06-developer/traceability-matrix.md`
- ownership: `../../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../../docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: produkt + tehnički vlasnik domena
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: bezbednosni vlasnik domena uz privatnost i audit podršku
- traceability signal: servis pokriva red Identitet i profil iz traceability matrice i mora emitovati samo centralno definisane profile i evidence statuse

## Readiness i release

- servis se otvara tek nakon potvrđenih ugovora i shared paketa
- servis mora dokumentovati audit, data-handling i manual-review posledice kada su relevantne
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
