# Model odobrenja za „MONTEZACIJA NAD MONTEZACIJAMA“

## Svrha

Ovaj dokument formalizuje kako se zahtev „DEVELOPER AND CREATE / VRH PROGRAMSKOG EKVIVALENTA / MONTEZACIJA NAD MONTEZACIJAMA“ uklapa u postojeći developer/create governance sloj kao krovni model odobrenja za objedinjavanje inovacija, paterna i tehničkih slojeva u jedinstven programski ekvivalent.

## Osnovna teza

- „MONTEZACIJA NAD MONTEZACIJAMA“ je meta-nivo montaže nad postojećim create governance okvirom, ne paralelni sistem
- inicijativa služi da objedini zahteve, domene, ownership, source-of-truth, ugovore, deljene modele, servise, aplikacije, testove, audit i release odluke pod jednim approval-ready narativom
- svaka inovacija ili patern koji želi da dobije status vrha programskog ekvivalenta mora prvo dokazati usklađenost sa centralnim developer/create slojem u `docs/06-developer/`

## Položaj u source-of-truth modelu

- centralni ulaz ostaje `docs/06-developer/README.md`
- fazna tehnička montaža ostaje zaključana kroz `program-equivalent-assembly-model.md`
- operativni redosled validacije i gate provere ostaje zaključan kroz `vrh-programskog-ekvivalenta-operativni-protokol.md`
- raspodela izvora istine ostaje zaključana kroz `source-of-truth-map.md`
- sledljivost od izvornog zahteva do testa i release odluke ostaje zaključana kroz `traceability-matrix.md`
- ovaj dokument ne redefiniše ownership, statuse, događaje, release nivoe niti readiness kriterijume, već propisuje kako se oni objedinjeno dokazuju kada se traži odobrenje za meta-nivo montaže

## Šta ulazi u vrh programskog ekvivalenta

U vrh programskog ekvivalenta ulaze samo artefakti i predlozi koji istovremeno pokazuju:

1. vezu ka izvornom strateškom, produktnom ili policy zahtevu
2. vezu ka create jezgru `profil → dokazi → procena → odluka → licenca → audit`
3. dokaz ownership-a za odluku, isporuku i kontrolu
4. vezu ka source-of-truth, traceability i release dokumentima
5. posledice po ugovorni, deljeni, servisni, aplikativni i test sloj
6. audit, manual-review, privatnost i regulatorne posledice kada su relevantne

## Approval-ready narativ

Zahtev za odobrenje mora jasno pokazati da se traži potvrda za objedinjavanje:

- inovacija i paterna kao kontrolisanih ulaza u sistem
- create domena i njihovih ownership granica
- API ugovora, deljenih modela i statusnog jezika
- servisnih granica, aplikativnih tokova i test posledica
- audit signala, release posledica i readiness dokaza

Narativ nije potpun ako opisuje samo ideju ili arhitektonski slogan bez dokaza da pogođeni slojevi mogu da naslede centralna pravila bez lokalne kontradikcije.

## Ownership pravilo za meta-nivo montaže

- vlasnik odluke ostaje kombinacija relevantnih vlasnika odluke iz pogođenih create domena
- vlasnik isporuke ostaje tehnički vlasnik sloja koji vodi objedinjavanje artefakata
- vlasnik kontrole ostaje najstroži relevantni primarni vlasnik kontrole iz pogođenih domena
- kada inicijativa seče više domena, ownership mora biti usklađen sa `create-domain-ownership-map.md` pre bilo kakvog spuštanja u niže slojeve
- nijedan approval zahtev ne može da zaobiđe postojeću ownership trojku: odluka, isporuka, kontrola

## Statusni jezik i događaji

- ovaj dokument ne uvodi nove statuse ni događaje
- važe centralni statusi i događaji iz `domain-status-and-events-catalog.md`
- svaki approval zahtev mora eksplicitno navesti koje domenske statuse, događaje i prelaze nasleđuje
- kada inicijativa utiče na više domena, koristi se zbir relevantnih centralnih statusa i događaja, bez lokalnih varijanti
- audit događaji, manual-review signali i regulatorne blokade ostaju obavezni tamo gde ih centralni katalog i kontrolni dokumenti već traže

## Obavezni stubovi procene

| Stub | Šta mora biti dokazano |
| --- | --- |
| Opseg | Koji artefakti, domeni i slojevi ulaze u meta-montažu i šta ostaje van opsega |
| Ownership | Ko potvrđuje odluku, ko vodi isporuku i ko nosi primarnu kontrolu |
| Statusni jezik | Koji postojeći statusi, događaji i prelazi stanja se nasleđuju |
| Traceability | Kako se ide od izvornog zahteva preko source-of-truth-a do ugovora, testova i release odluke |
| Kontrole | Bezbednost, privatnost, audit, manual review i regulatorne blokade |
| Release spremnost | Koji readiness, done i release gate kriterijumi važe pre otvaranja izvršnog sloja |

## Faze meta-montaže

1. potvrda značenja, cilja i granica inicijative
2. mapiranje svih relevantnih inovacija i paterna na postojeće create domene
3. usklađivanje ownership-a, statusa, događaja i kontrolnih posledica
4. povezivanje sa ugovornim, deljenim, servisnim, aplikativnim i test slojem
5. potvrda readiness, definition-of-done i release gate kriterijuma za svaku zavisnu oblast

## Obavezna gate validacija pre finalnog odobrenja

- finalna VRH potvrda može biti doneta tek nakon redosleda `definition-of-ready.md` → `definition-of-done.md` → `release-gates.md`
- predlog se odbija ili vraća na dopunu kada uvodi lokalna značenja, lokalne statuse/događaje ili zaobilazi centralni source-of-truth i ownership model
- kontrolni zaključak mora pokazati da ne postoji kontradikcija između `docs/`, `specs/api/`, `packages/`, `services/`, `apps/` i `tests/` slojeva

## Očekivani deliverable-i

- krovni opis inicijative i razlog odobrenja
- mapa inovacija i paterna prema create jezgru
- veza sa ownership mapom, source-of-truth mapom i modelom montaže programskog ekvivalenta
- spisak zavisnih tehničkih artefakata koje inicijativa otvara, menja ili blokira
- kriterijumi za odobrenje, odbijanje ili vraćanje na dopunu

## Kriterijumi za odobrenje

Inicijativa može biti odobrena samo ako:

- ne uvodi paralelni governance sistem van `docs/06-developer/`
- ne redefiniše ownership, statusni jezik ili release pravila mimo centralnih dokumenata
- pokazuje vezu sa create jezgrom `profil → dokazi → procena → odluka → licenca → audit`
- pokazuje traceability od izvornog zahteva do ugovora, testova i release odluke
- pokazuje kako pogođeni slojevi nasleđuju iste kontrolne stubove bez spuštanja nivoa kontrole

## Razlozi za odbijanje ili vraćanje na dopunu

- predlog tvrdi da je vrh programskog ekvivalenta, ali nema dokaz source-of-truth usklađenosti
- predlog otvara servisni, aplikativni ili test sloj bez prethodno potvrđenih ugovora i shared jezika
- predlog uvodi lokalne statuse, događaje, ownership granice ili release pravila
- predlog ne pokazuje audit, manual-review ili regulatorne posledice kada su relevantne
- predlog ne može da mapira inovacije i paterne na prioritete create jezgra

## Rizici i ograničenja

- nije dozvoljeno lokalno redefinisanje značenja mimo `docs/06-developer/`
- nije dozvoljeno otvaranje servisa, aplikacija ili test proširenja bez prethodno zaključenih ugovora i shared jezika
- nije dozvoljeno uvođenje novih statusa, događaja ili ownership granica mimo centralnih dokumenata
- višedomenski artefakti moraju naslediti najstroži relevantni skup kontrola

## Mera uspeha

- inicijativa je uspešna tek kada objedinjeno povezuje inovacije i paterne sa create jezgrom `profil → dokazi → procena → odluka → licenca → audit`
- svaki budući tehnički sloj mora moći da pokaže vezu ka ovom krovnom modelu bez kontradikcije sa postojećim governance dokumentima
- repozitorijum zadržava jedan centralni developer/create okvir, dok „MONTEZACIJA NAD MONTEZACIJAMA“ služi kao krovni approval model za njegovo kontrolisano objedinjavanje
