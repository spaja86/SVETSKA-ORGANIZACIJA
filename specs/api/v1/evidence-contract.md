# Ugovor: dokazi

## Izvor i ownership

- izvorni dokumenti: `docs/03-product/product-requirements.md`, `docs/04-policies/data-governance.md`
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
- vlasnik kontrole: bezbednosni vlasnik domena uz privatnost, retenciju i audit podršku

## Resurs
- dokaz kompetencije

## Ključne operacije
- unos dokaza
- pregled istorije dokaza
- promena validnosti ili statusa dokaza

## Kontrole
- validacija formata, porekla i povezanosti sa profilom
- retencija i minimizacija podataka
- audit događaji za unos i odbijanje
- ručna revizija kada dokaz nosi visok regulatorni rizik

## Audit, manual review i test posledice
- audit posledice: svaki zahtev, promena statusa, ručna odluka, regulatorna blokada i izuzetak moraju ostaviti korelisan trag
- manual review: obavezan kada dokaz zahteva ručnu proveru porekla, validnosti ili regulatorni izuzetak
- test posledice: `tests/contract/README.md`, `tests/domain/README.md`, `tests/integration/README.md`, `tests/audit/README.md`

## Klase grešaka
- `validation-error`
- `authorization-error`
- `regulatory-block`
- `review-required`

## Test fokus
- negativni scenariji za nekompletan dokaz
- poreklo i veza sa profilom
- audit za unos, odbijanje i vraćanje na dopunu
