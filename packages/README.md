# Paketi

Ovde se nalaze deljeni modeli domena, validaciona pravila, statusi i pomoćne biblioteke.

## Aktivni skelet

- `domain-profile/` — modeli profila, dokaza i identiteta
- `domain-assessment/` — modeli procene, rezultata i žalbi
- `domain-license/` — modeli licenci, statusa i obnove
- `domain-partner/` — modeli partnera, angažmana i potvrda
- `domain-audit/` — audit događaji, korelacija i KPI signali
- `domain-regulatory/` — pravila jurisdikcija, ograničenja i izuzeci
- `shared-statuses/` — zajednički statusi i pravila prelaza
- `shared-validation/` — deljene validacije i kontrolna pravila

## Centralna governance veza

- centralni ulaz: `../docs/06-developer/README.md`
- source-of-truth: `../docs/06-developer/source-of-truth-map.md`, `../docs/06-developer/domain-status-and-events-catalog.md`, `../docs/06-developer/error-taxonomy.md`
- ownership: `../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../docs/06-developer/traceability-matrix.md`

## Pravilo deljenog domena

- domenska pravila se definišu jednom i koriste kroz aplikacije i servise
- paketi čuvaju jedinstveni jezik domena i sprečavaju dupliranje značenja
- svaki deljeni model mora imati jasnu vezu sa izvorom zahteva, ownership-om, ugovorom i testovima
- referentni statusi, događaji i greške usklađuju se sa `../docs/06-developer/README.md`

## Ownership i kontrola

- vlasnici odluke: odgovarajući domenski ili višedomenski vlasnici iz `../docs/06-developer/create-domain-ownership-map.md`
- vlasnik isporuke: tehnički vlasnik implementacije paketa
- vlasnik kontrole: najstroži relevantni vlasnik kontrole za deljeni ili domenski sloj
- traceability signal: svaki paket mora odražavati relevantne redove iz `../docs/06-developer/traceability-matrix.md`

## Readiness i release

- `../packages/` se otvara zajedno sa `../specs/api/` slojem pre izvršnih servisa i aplikacija
- shared paketi ne uvode nova pravila bez centralne dopune source-of-truth i ownership dokumenata
- završna spremnost paketa proverava se kroz `../docs/06-developer/definition-of-ready.md`, `../docs/06-developer/definition-of-done.md` i `../docs/06-developer/release-gates.md`
