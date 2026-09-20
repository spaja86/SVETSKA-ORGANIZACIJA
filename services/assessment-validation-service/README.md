# Assessment validation service

## Svrha

Servis za procenu, rezultat, ljudsku reviziju i korektivni tok odluke.

## Ulazi i izlazi

- ulazi: profil, dokazi, kriterijumi procene, partner ili admin intervencija
- izlazi: preliminarni i potvrđeni rezultat, signal za žalbu, signal za ručnu reviziju

## Granice odgovornosti

- upravlja procenom i odlukom
- ne izdaje licencu niti menja regulatorna pravila bez zavisnih servisa
- ne redefiniše shared statuse, događaje ili greške

## Povezani artefakti

- `specs/api/v1/assessment-contract.md`
- `packages/domain-assessment/`
- `packages/shared-statuses/`
- `docs/06-developer/manual-review-checkpoints.md`
- `tests/domain/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/manual-review-checkpoints.md`, `docs/06-developer/ai-governance-plan.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: produkt + policy + tehnički vlasnik
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: AI governance vlasnik domena uz policy i audit podršku
- traceability signal: servis pokriva red Procena i validacija i mora zadržati trag odluke, žalbe i ljudske supervizije

## Readiness i release

- servis se otvara tek nakon potvrđenih ugovora i shared paketa
- servis mora dokumentovati audit, data-handling i manual-review posledice kada su relevantne
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
