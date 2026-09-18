# Katalog statusa i događaja po domenima

## Svrha

Ovaj katalog uvodi zajednički jezik za statuse, događaje i prelaze stanja kroz create tok.

## Identitet i profil

### Statusi
- draft
- active
- pending-review
- suspended
- archived

### Događaji
- profile.created
- profile.updated
- evidence.submitted
- evidence.rejected
- profile.status.changed

## Procena i validacija

### Statusi
- requested
- in-review
- awaiting-human-review
- approved
- rejected
- appealed

### Događaji
- assessment.requested
- assessment.started
- assessment.result.recorded
- assessment.human-review.requested
- assessment.decision.confirmed
- assessment.appeal.opened

## Licence

### Statusi
- pending-issuance
- active
- rejected
- suspended
- expired
- renewal-pending

### Događaji
- license.issuance.requested
- license.issued
- license.rejected
- license.suspended
- license.renewal.requested
- license.status.changed

## Partneri i angažmani

### Statusi
- invited
- active
- restricted
- inactive

### Događaji
- partner.accredited
- partner.assigned
- engagement.confirmed
- engagement.disputed

## Audit i KPI

### Statusi
- recorded
- correlated
- flagged
- exported

### Događaji
- audit.event.recorded
- audit.trace.correlated
- kpi.metric.emitted
- audit.exception.flagged

## Regulatorna pravila

### Statusi
- draft
- active
- superseded
- blocked

### Događaji
- rule.created
- rule.activated
- rule.exception.applied
- jurisdiction.blocked

## Pravilo održavanja

- novi status ili događaj mora imati domensku referencu i test posledicu
- promena kataloga proverava se zajedno sa ugovorima, audit zahtevima i traceability matricom
