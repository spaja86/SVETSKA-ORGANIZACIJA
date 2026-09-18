# Pregled spremnosti modula

## Svrha

Ovaj pregled pokazuje šta svaki sloj mora imati pre prelaska iz dokumentacionog skeleta u izvršnu implementaciju.

## Readiness po slojevima

| Sloj | Trenutno stanje | Obavezno pre implementacije | Dokaz spremnosti |
| --- | --- | --- | --- |
| `docs/` | aktivan i centralizovan | source-of-truth, ownership, faze i otvorene odluke | developer indeks + povezani governance dokumenti |
| `apps/` | skelet README portala | minimalni ekrani, uloge, događaji i zavisni ugovori | README po portalu |
| `services/` | skelet README servisa | ulazi, izlazi, statusi, događaji, zabrane preklapanja | README po servisu |
| `packages/` | skelet README paketa | entiteti, validacije, statusi, ugovorne veze | README po paketu |
| `specs/api/` | v1 minimalni ugovori | standard grešaka, metadata, traceability i ownership | `specs/api/README.md` + `specs/api/v1/*.md` |
| `tests/` | skelet test slojeva | negativni scenariji, autorizacija, regulatorne blokade, audit verifikacija | README po test sloju |

## Pravilo prelaza

- sloj ne prelazi u sledeću fazu dok njegov dokaz spremnosti nije ažuran
- kada jedan sloj promeni status, zavisni slojevi proveravaju svoju usklađenost
- readiness nije dovoljan za release bez prolaska kroz `release-gates.md`
