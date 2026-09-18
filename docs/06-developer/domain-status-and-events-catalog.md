# Katalog statusa i događaja po domenima

## Svrha

Ovaj katalog uvodi zajednički jezik za statuse, događaje i prelaze stanja kroz create tok.

## Pravilo standarda

- statusi predstavljaju poslovno stanje resursa, ne tehničko stanje procesa
- događaji koriste standard iz `event-naming-standard.md`
- svaki novi status ili događaj mora navesti dozvoljene prelaze, audit posledicu i test fokus

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

### Dozvoljeni prelazi
- `draft -> active`
- `active -> pending-review`
- `active -> suspended`
- `suspended -> active`
- `active -> archived`

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

### Dozvoljeni prelazi
- `requested -> in-review`
- `in-review -> awaiting-human-review`
- `in-review -> approved`
- `in-review -> rejected`
- `awaiting-human-review -> approved`
- `awaiting-human-review -> rejected`
- `approved -> appealed`
- `rejected -> appealed`

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

### Dozvoljeni prelazi
- `pending-issuance -> active`
- `pending-issuance -> rejected`
- `active -> renewal-pending`
- `active -> suspended`
- `active -> expired`
- `renewal-pending -> active`
- `suspended -> active`

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

### Dozvoljeni prelazi
- `invited -> active`
- `active -> restricted`
- `restricted -> active`
- `active -> inactive`

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

### Dozvoljeni prelazi
- `recorded -> correlated`
- `recorded -> flagged`
- `correlated -> exported`
- `flagged -> correlated`

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

### Dozvoljeni prelazi
- `draft -> active`
- `active -> superseded`
- `active -> blocked`
- `blocked -> active`

## Pravilo održavanja

- novi status ili događaj mora imati domensku referencu i test posledicu
- promena kataloga proverava se zajedno sa ugovorima, audit zahtevima i traceability matricom
- visoko-rizični događaji moraju imati ručnu reviziju definisanu u `manual-review-checkpoints.md`
