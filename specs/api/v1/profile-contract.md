# Ugovor: profil

## Izvor i ownership

- izvorni dokumenti: `docs/03-product/product-requirements.md`, `docs/02-platform/domain-model.md`
- domen: identitet i profil
- povezani moduli: `apps/user-portal/`, `services/profile-identity-service/`, `packages/domain-profile/`

## Governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/api-contract-governance.md`, `docs/06-developer/domain-status-and-events-catalog.md`, `docs/06-developer/error-taxonomy.md`
- traceability: `docs/06-developer/traceability-matrix.md`
- repo-wide radni takt: zahtev → domen → odluka → ugovor i deljeni modeli → test posledice → audit i usklađenost → implementacija → verifikacija i release odluka

## Ownership trojka

- vlasnik odluke: produkt + tehnički vlasnik domena
- vlasnik isporuke: tehnički vlasnik implementacije ugovora i zavisnih modula
- vlasnik kontrole: bezbednosni vlasnik domena uz privatnost i audit podršku

## Resurs
- profil korisnika

## Ključne operacije
- kreiranje profila
- pregled profila
- promena statusa profila
- pregled istorije promena

## Statusi
- `draft`
- `active`
- `pending-review`
- `suspended`
- `archived`

## Kontrole
- obavezna polja i validacija identiteta
- audit događaji za kreiranje i promenu statusa
- kontrola pristupa po ulozi
- povezivanje sa dokazima i istorijom profila

## Audit, manual review i test posledice
- audit posledice: svaki zahtev, promena statusa, ručna odluka, regulatorna blokada i izuzetak moraju ostaviti korelisan trag
- manual review: obavezan kada dokaz, identitet ili korekcija traže ručnu potvrdu ili žalbeni tok
- test posledice: `tests/contract/README.md`, `tests/domain/README.md`, `tests/integration/README.md`, `tests/audit/README.md`

## Klase grešaka
- `validation-error`
- `authorization-error`
- `conflict-error`
- `not-found`

## Test fokus
- validacija kreiranja profila
- zabrana nevažećih promena statusa
- istorija promena i audit događaja
