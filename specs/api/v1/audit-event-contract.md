# Ugovor: audit događaj

## Izvor i ownership

- izvorni dokumenti: `docs/05-operations/kpi-framework.md`, `docs/04-policies/data-governance.md`
- domen: audit i KPI
- povezani moduli: `apps/admin-portal/`, `services/audit-reporting-service/`, `packages/domain-audit/`

## Governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/api-contract-governance.md`, `docs/06-developer/domain-status-and-events-catalog.md`, `docs/06-developer/error-taxonomy.md`
- traceability: `docs/06-developer/traceability-matrix.md`
- repo-wide radni takt: zahtev → domen → odluka → ugovor i deljeni modeli → test posledice → audit i usklađenost → implementacija → verifikacija i release odluka

## Ownership trojka

- vlasnik odluke: operativni + tehnički vlasnik domena
- vlasnik isporuke: tehnički vlasnik implementacije ugovora i zavisnih modula
- vlasnik kontrole: audit, bezbednosni i data-governance vlasnik

## Resurs
- audit događaj

## Ključne operacije
- evidentiranje događaja
- korelacija po korisniku, odluci i jurisdikciji
- izdvajanje KPI ulaza
- označavanje incidenta ili neuspele korelacije

## Status ili razlog
- status nije primenljiv kao primarni atribut resursa; kanonski signal nose tip događaja, korelacioni identifikator i rezultat obrade
- neuspešna obrada, incident i regulatorni izuzetak moraju imati eksplicitan razlog i korelaciju sa create korakom

## Kontrole
- neizmenjivost traga
- povezanost sa create korakom i statusom
- signal za incidente i neuspele korelacije
- standardizovana metadata događaja

## Audit, manual review i test posledice
- audit posledice: svaki zahtev, promena statusa, ručna odluka, regulatorna blokada i izuzetak moraju ostaviti korelisan trag
- manual review: obavezan kada događaj označava incident, neuspelu korelaciju ili regulatorni izuzetak
- test posledice: `tests/contract/README.md`, `tests/integration/README.md`, `tests/audit/README.md`

## Klase grešaka
- `validation-error`
- `not-found`
- `internal-integrity-error`

## Test fokus
- potpuna korelacija create toka
- neuspele korelacije i incident signal
- KPI emitovanje za ključne odluke
