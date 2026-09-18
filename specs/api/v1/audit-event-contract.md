# Ugovor: audit događaj

## Izvor i ownership

- izvorni dokumenti: `docs/05-operations/kpi-framework.md`, `docs/04-policies/data-governance.md`
- domen: audit i KPI
- povezani moduli: `apps/admin-portal/`, `services/audit-reporting-service/`, `packages/domain-audit/`

## Resurs
- audit događaj

## Ključne operacije
- evidentiranje događaja
- korelacija po korisniku, odluci i jurisdikciji
- izdvajanje KPI ulaza
- označavanje incidenta ili neuspele korelacije

## Kontrole
- neizmenjivost traga
- povezanost sa create korakom i statusom
- signal za incidente i neuspele korelacije
- standardizovana metadata događaja

## Klase grešaka
- `validation-error`
- `not-found`
- `internal-integrity-error`

## Test fokus
- potpuna korelacija create toka
- neuspele korelacije i incident signal
- KPI emitovanje za ključne odluke
