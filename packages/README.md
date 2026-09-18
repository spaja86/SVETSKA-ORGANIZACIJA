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

## Pravilo deljenog domena

- domenska pravila se definišu jednom i koriste kroz aplikacije i servise
- paketi čuvaju jedinstveni jezik domena i sprečavaju dupliranje značenja
- svaki deljeni model mora imati jasnu vezu sa izvorom zahteva, ugovorom i testovima
