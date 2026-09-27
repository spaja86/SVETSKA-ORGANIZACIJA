# Model montaže programskog ekvivalenta

## Svrha

Ovaj dokument formalizuje kako se postojeći developer/create governance okvir sklapa u stvarni programski ekvivalent repozitorijuma bez lokalnog redefinisanja značenja, ownership-a i kontrola.

## Šta je vrh programskog ekvivalenta

- vrh programskog ekvivalenta je centralno zaključan tehnički lanac koji povezuje zahtev, domen, ownership, source-of-truth, ugovor, deljene modele, servisne granice, aplikativne tokove, testove, audit i release odluku
- taj lanac počinje u `README.md`, `docs/README.md` i pre svega u `docs/06-developer/README.md`, ali jedino `docs/06-developer/` zaključava značenje koje sme da se spusti u ostale slojeve
- nijedan izvršni, ugovorni ili test artefakt ne uvodi lokalno pravilo ako njegov red u ovom lancu nije prethodno zatvoren kroz centralni developer/create sloj

## Obavezni tehnički lanac

1. zahtev dobija referencu na izvorni strateški, produktni ili policy dokument
2. potvrđuje se domen i ownership trojka: odluka, isporuka, kontrola
3. proverava se source-of-truth i po potrebi menja prvo centralni dokument
4. zaključavaju se ugovori, statusi, događaji, greške i deljeni modeli
5. potvrđuju se servisne granice, zabrane preklapanja i regulatorne blokade
6. otvaraju se aplikativni tokovi, uloge i pristupne kontrole
7. određuju se test posledice, audit signal i release posledice
8. implementacija počinje tek nakon readiness potvrde
9. završetak ide kroz definition-of-done i release gate proveru

## Pravilo montaže slojeva

- montaža je fazno sklapanje `docs/`, `specs/api/`, `packages/`, `services/`, `apps/` i `tests/` oko create jezgra, ne paralelno nasumično otvaranje modula
- svaki niži sloj nasleđuje centralne odluke i prikazuje ih kroz svoj README, ugovor ili test signal
- ako sloj ne može da pokaže source-of-truth, ownership, traceability i kontrolne stubove, njegovo otvaranje se zaustavlja
- deljeni i višedomenski artefakti primenjuju najstroži skup relevantnih kontrola

## Repo-wide prioritet jezgra

- jedini prioritet prvog talasa ostaje create jezgro `profil → dokazi → procena → odluka → licenca → audit`
- sekundarni tokovi, dodatne integracije i lokalizacija ne dobijaju prioritet dok jezgro nema stabilne ugovore, statuse, događaje, audit trag i release kontrolu
- svaki novi artefakt mora dokazati da direktno podržava ovo jezgro ili ostaje van opsega trenutnog talasa

## Minimalni slojni ekvivalent create jezgra

Sledeća mapa opisuje koje vrste slojeva moraju postojati za svaki prioritetni create korak. Konkretna imena artefakata i direktorijuma održavaju se kroz ownership mapu, ugovorne README indekse i module readiness dokumente.

| Create korak | Ugovorni sloj | Deljeni sloj | Servisni sloj | Aplikativni sloj | Test signal |
| --- | --- | --- | --- | --- | --- |
| Profil | ugovor za profil i status profila | modeli profila, identiteta i osnovnih validacija | servis koji upravlja profilom i identitetom | korisnički portal za unos i pregled | domenska i integraciona validacija |
| Dokazi | ugovor za dokaz i istoriju dokaza | modeli dokaza i deljene validacije | servis za prihvat, proveru i evidenciju dokaza | korisnički portal za predaju i korekciju | domenska i ugovorna validacija |
| Procena | ugovor za zahtev procene i rezultat | modeli procene, kriterijuma i rezultata | servis procene i validacije | partnerski ili administrativni portal za obradu | domenska i integraciona validacija |
| Odluka | ugovor za potvrdu rezultata, žalbu i korekciju | modeli odluke, statusa i ručne revizije | servis koji zaključava ishod procene | partnerski ili administrativni portal za potvrdu | domenska i audit validacija |
| Licenca | ugovor za izdavanje, status i obnovu licence | modeli licence, statusa i pravila prelaza | servis za izdavanje i upravljanje licencom | korisnički i partnerski portal za pregled i radnju | ugovorna i integraciona validacija |
| Audit | ugovor za audit događaj i KPI ulaze | modeli audit događaja i korelacije | audit i reporting servis | administrativni portal za trag i nadzor | audit i integraciona validacija |

## Obavezni kontrolni stubovi

- role-based pristup
- audit trag za svaku odluku, promenu statusa i izuzetak
- manual review za visoko-rizične odluke i regulatorno osetljive tokove
- žalbeni i korektivni tok kada se menja status ili ishod
- klasifikacija podataka, minimizacija i retencija
- release gate provera pre prelaza između slojeva

## Faze sklapanja

1. zaključavanje governance-a, ownership-a i source-of-truth raspodele u `docs/06-developer/`
2. potvrda create opsega i prioriteta jezgra
3. zaključavanje statusa, događaja, grešaka i shared jezika
4. otvaranje `specs/api/` i `packages/` kao ugovornog i deljenog sloja
5. otvaranje `services/` tek nakon potvrđenih ugovora, shared modela i kontrola
6. otvaranje `apps/` tek nakon potvrđenih servisnih granica, uloga i pristupnih tačaka
7. paralelno širenje `tests/` uz svaki novi ugovor, status, događaj i audit signal
8. stabilizacija kroz readiness, done i release kontrole pre širenja na sekundarne tokove

## Pravilo zabrane lokalnog značenja

- `specs/api/` ne uvodi ownership granice ili statusni jezik mimo centralnih dokumenata
- `packages/` ne uvode nova pravila bez dopune source-of-truth i ownership sloja
- `services/` ne uvode lokalne event ili status varijante mimo centralnog kataloga
- `apps/` ne definišu domenska pravila koja pripadaju ugovorima, paketima ili servisima
- `tests/` ne uvode alternativni kriterijum istine mimo centralnih governance i ugovornih artefakata

## Mera uspeha

- nijedna tehnička promena ne nastaje van centralnog developer/create okvira
- svaki sloj koristi isti ownership model, statusni jezik i release pravila
- svaki create korak ima vezu između zahteva, ugovora, paketa, servisa, aplikacija, testova i audit traga
- repozitorijum se ponaša kao jedinstven product-engineering sistem za create jezgro
