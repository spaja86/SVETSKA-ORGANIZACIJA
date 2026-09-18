# Matrica rizika za create tok

| Rizik | Gde nastaje | Posledica | Kontrola |
| --- | --- | --- | --- |
| Nekompletan profil | kreiranje profila | pogrešna procena ili blokirana licenca | obavezna polja, validacija unosa, audit otvaranja |
| Nevažeći ili sporni dokaz | unos dokaza | pogrešna odluka ili žalba | validacija porekla, status dokaza, retencija i review |
| Automatizovana odluka bez ljudske provere | procena | bezbednosni, etički i regulatorni rizik | obavezna ljudska revizija za visoko-rizične slučajeve |
| Nevažeći prelaz statusa licence | izdavanje i obnova | regulatorna neusaglašenost | katalog statusa, ugovorna validacija, negativni testovi |
| Nedovoljna kontrola pristupa | pregled statusa ili admin tokovi | curenje podataka i neovlašćen pristup | role-based pristup, audit događaji, minimalne dozvole |
| Nedostajući audit trag | bilo koji create korak | nemogućnost dokazivanja odluke | obavezni audit događaji i korelacija po toku |
| Lokalno pravilo nije primenjeno | regulatorni korak | pogrešno izdavanje ili blokada | eksplicitna pravila jurisdikcije i release gate provera |
| Nepovezani zahtevi, ugovori i testovi | prelaz iz dokumentacije u implementaciju | nekonzistentna izgradnja | traceability matrica i definition-of-done provera |
