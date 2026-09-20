# Partner engagement service

## Svrha

Servis za partnere, angažmane, potvrde i operativnu koordinaciju partner toka.

## Ulazi i izlazi

- ulazi: partner profil, angažman, potvrda učinka, sporni slučaj
- izlazi: partner status, potvrda angažmana, audit signal partner akcije

## Granice odgovornosti

- upravlja partnerima i angažmanima
- ne menja rezultate procene ili licencu bez zavisnih ugovora
- ne redefiniše ownership granice iz create-domain-ownership-map.md

## Povezani artefakti

- `specs/api/v1/partner-contract.md`
- `packages/domain-partner/`
- `tests/integration/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/external-integration-map.md`, `docs/06-developer/role-permission-model.md`, `docs/06-developer/create-domain-ownership-map.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: operativni + tehnički vlasnik
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: operativni kontrolni vlasnik partnera uz audit i policy podršku
- traceability signal: servis pokriva red Partneri i angažmani i mora čuvati trag partner potvrda i spornih angažmana

## Readiness i release

- servis se otvara tek nakon potvrđenih ugovora i shared paketa
- servis mora dokumentovati audit, data-handling i manual-review posledice kada su relevantne
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
