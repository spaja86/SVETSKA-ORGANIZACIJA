# Pregled spremnosti modula

## Svrha

Ovaj pregled pokazuje šta svaki sloj mora imati pre prelaska iz dokumentacionog skeleta u izvršnu implementaciju.

## Readiness po slojevima

| Sloj | Trenutno stanje | Obavezno pre implementacije | Otvaranje zavisi od | Dokaz spremnosti |
| --- | --- | --- | --- | --- |
| `docs/` | aktivan i centralizovan | source-of-truth, ownership, faze, release nivo i otvorene odluke | nema prethodnog sloja; ovo je ulazni kontrolni sloj | developer indeks + povezani governance dokumenti |
| `apps/` | skelet README portala | minimalni ekrani, uloge, događaji, ownership, zavisni ugovori i kontrolne tačke pristupa | potvrđeni `services/`, `specs/api/` i `packages/` artefakti za tok koji aplikacija koristi | README po portalu + veza ka traceability matrici |
| `services/` | skelet README servisa | ulazi, izlazi, statusi, događaji, ownership, zabrane preklapanja i regulatorne blokade | potvrđeni `specs/api/` i `packages/` artefakti, plus zaključan `docs/` governance | README po servisu + veza ka source-of-truth-u |
| `packages/` | skelet README paketa | entiteti, validacije, statusi, ownership, ugovorne veze i zajednički jezik domena | zaključan `docs/` governance i potvrđen create opseg | README po paketu + veza ka ownership mapi |
| `specs/api/` | v1 minimalni ugovori | standard grešaka, metadata, traceability, ownership, audit posledice i manual-review signal | zaključan `docs/` governance i potvrđen create opseg | `specs/api/README.md` + `specs/api/v1/*.md` |
| `tests/` | skelet test slojeva | negativni scenariji, autorizacija, regulatorne blokade, audit verifikacija, ownership signal i fazni dokaz pokrivenosti | odgovarajući ugovori, statusi, događaji i sloj koji test potvrđuje | README po test sloju + veza ka release kontroli |

## Obavezni README minimum po sloju

- veza ka `docs/06-developer/README.md`
- reference na source-of-truth, ownership i traceability dokumente
- jasan domen ili izjava da artefakt nasleđuje višedomenski ownership
- readiness i release očekivanja za naredni korak otvaranja sloja
- audit, data-handling i manual-review posledice kada su relevantne

## Redosled otvaranja slojeva

1. `docs/` mora zaključati značenje i ownership pre bilo kog drugog sloja
2. `specs/api/` i `packages/` otvaraju se pre izvršnih servisa kada menjaju ugovore ili deljeni jezik domena
3. `services/` se otvaraju tek kada su zavisni paketi, ugovori i kontrole spremni
4. `apps/` se otvaraju tek kada su potvrđeni poslovni tokovi, uloge i zavisni interfejsi
5. `tests/` se šire paralelno sa svakim novim ugovorom, statusom, događajem ili kontrolom

## Pravilo prelaza

- sloj ne prelazi u sledeću fazu dok njegov dokaz spremnosti nije ažuran
- kada jedan sloj promeni status, zavisni slojevi proveravaju svoju usklađenost
- readiness nije dovoljan za release bez prolaska kroz `release-gates.md`
- dokumentaciona spremnost prethodi svakoj tehničkoj realizaciji, čak i kada je promena ograničena na skelet direktorijuma
