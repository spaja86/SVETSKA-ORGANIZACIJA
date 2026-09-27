# Ugovor: procena

## Izvor i ownership

- izvorni dokumenti: `docs/03-product/use-cases-and-user-journeys.md`, `docs/04-policies/security-ethics-and-compliance.md`
- domen: procena i validacija
- povezani moduli: `apps/partner-portal/`, `apps/admin-portal/`, `services/assessment-validation-service/`, `packages/domain-assessment/`

## Governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/api-contract-governance.md`, `docs/06-developer/domain-status-and-events-catalog.md`, `docs/06-developer/error-taxonomy.md`
- traceability: `docs/06-developer/traceability-matrix.md`
- repo-wide radni takt: zahtev → domen → odluka → ugovor i deljeni modeli → test posledice → audit i usklađenost → implementacija → verifikacija i release odluka

## Ownership trojka

- vlasnik odluke: produkt + policy + tehnički vlasnik domena
- vlasnik isporuke: tehnički vlasnik implementacije ugovora i zavisnih modula
- vlasnik kontrole: bezbednosni i audit vlasnik uz manual-review kontrolu za visokorizične odluke

## Resurs
- zahtev za procenu i rezultat

## Ključne operacije
- otvaranje zahteva za procenu
- evidentiranje rezultata
- potvrda ljudske revizije i žalbe
- potvrda konačne odluke

## Statusi
- `requested`
- `in-review`
- `awaiting-human-review`
- `approved`
- `rejected`
- `appealed`

## Kontrole
- audit trag za odluku i ručnu superviziju
- jasno razdvajanje preliminarne i konačne odluke
- manual review checkpoint za visokorizične odluke

## Audit, manual review i test posledice
- audit posledice: svaki zahtev, promena statusa, ručna odluka, regulatorna blokada i izuzetak moraju ostaviti korelisan trag
- manual review: obavezan za visokorizične procene, override odluke i žalbene tokove
- test posledice: `tests/contract/README.md`, `tests/domain/README.md`, `tests/integration/README.md`, `tests/audit/README.md`

## Klase grešaka
- `validation-error`
- `authorization-error`
- `review-required`
- `internal-integrity-error`

## Test fokus
- pozitivni i negativni scenariji procene
- žalbeni tok i override
- korelacija sa dokazima i licencom
