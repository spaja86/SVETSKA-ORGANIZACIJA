# Ugovor: licenca

## Izvor i ownership

- izvorni dokumenti: `docs/02-platform/global-work-licenses.md`, `docs/03-product/product-requirements.md`
- domen: licence
- povezani moduli: `apps/user-portal/`, `services/license-service/`, `packages/domain-license/`

## Governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/api-contract-governance.md`, `docs/06-developer/domain-status-and-events-catalog.md`, `docs/06-developer/error-taxonomy.md`
- traceability: `docs/06-developer/traceability-matrix.md`
- repo-wide radni takt: zahtev → domen → odluka → ugovor i deljeni modeli → test posledice → audit i usklađenost → implementacija → verifikacija i release odluka

## Ownership trojka

- vlasnik odluke: produkt + policy + tehnički vlasnik domena
- vlasnik isporuke: tehnički vlasnik implementacije ugovora i zavisnih modula
- vlasnik kontrole: regulatorni i bezbednosni vlasnik domena uz audit podršku

## Resurs
- licenca i status licence

## Ključne operacije
- izdavanje licence
- pregled statusa licence
- obnova, suspenzija i odbijanje
- pregled istorije statusa

## Statusi
- `pending-issuance`
- `active`
- `rejected`
- `suspended`
- `expired`
- `renewal-pending`

## Kontrole
- validni prelazi statusa
- regulatorne blokade i ovlašćenja
- audit događaji za svaku promenu statusa
- ručna potvrda kada procena ili pravila nisu jednoznačni

## Audit, manual review i test posledice
- audit posledice: svaki zahtev, promena statusa, ručna odluka, regulatorna blokada i izuzetak moraju ostaviti korelisan trag
- manual review: obavezan kada procena ili regulatorna pravila ne daju jednoznačnu odluku
- test posledice: `tests/contract/README.md`, `tests/domain/README.md`, `tests/integration/README.md`, `tests/audit/README.md`

## Klase grešaka
- `authorization-error`
- `regulatory-block`
- `conflict-error`
- `review-required`

## Test fokus
- validni i nevalidni prelazi statusa
- blokade po jurisdikciji
- audit za izdavanje, odbijanje i suspenziju
