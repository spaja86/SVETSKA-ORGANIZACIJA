# Servisi

Ovde se nalaze planirane servisne granice, integracioni slojevi i kontrolni servisi.

## Aktivni skelet

- `profile-identity-service/` — profil, identitet i dokazi
- `assessment-validation-service/` — procena, rezultat i ljudska revizija
- `license-service/` — izdavanje, status i obnova licence
- `partner-engagement-service/` — partneri, angažmani i potvrde
- `audit-reporting-service/` — audit događaji, korelacija i KPI ulazi
- `regulatory-rules-service/` — lokalna pravila, blokade i izuzeci

## Pravilo granica

- servisi nose izvršavanje domena i integracija, ali ne redefinišu deljene modele van `packages/`
- svaki servis mora imati eksplicitne ulaze, izlaze, statuse i audit događaje
- regulatorna pravila i kontrole pristupa moraju biti ugrađeni u dizajn servisa od početka
