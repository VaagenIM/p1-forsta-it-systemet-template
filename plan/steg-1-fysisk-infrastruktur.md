# Steg 1 – fysisk infrastruktur og kommunikasjon

**Arbeidsplan:** [Forstå IT-systemet](arbeidsplan.md)
**Startside:** [Forstå IT-systemet](../README.md)
**Dager:** [Mandag](#mandag) · [tirsdag](#tirsdag) · [onsdag](#onsdag) · [torsdag](#torsdag) · [fredag](#fredag)

**Ukemål:** Identifisere fysiske komponenter, roller og forbindelser og forklare hvordan en klient kobles til nettverket.

**Ressurser:** [NDLA-fagstoff for perioden](../ressurser/ndla-fagstoff.md) · [Programvare og verktøy](../ressurser/programvare.md) · [Nettverksmodeller](../ressurser/nettverksmodeller.md)

**Muntlig gjennomgang:** Du får vite hvilken stasjon og klient du skal bruke, hvilke deler av IT-laben som inngår, og hvilke systemnavn og nettverksverdier du kan dokumentere.

**Før du begynner:** Gjennomfør [startsjekken](../ressurser/programvare.md#startsjekk). Bruk støtteveien der før du går videre hvis noe mangler.

## Mandag

**Dagens tema:** Datamaskinen og dokumentasjonsstrukturen. Du skal forstå hva klienten består av, og hvor arbeidet skal dokumenteres.

**Dagens arbeid:** Åpne Classroom50-invitasjonen i Teams-kanalen, kontroller at elevrepoet er privat, og klon det med Git i terminalen. Åpne deretter mappen i VS Code. Skriv planen i delen `Min arbeidsprosess` i systemoversikten før du undersøker klienten og utstyret ved egen stasjon: PC, hovedkort, CPU, RAM, lagring, nettverkskort (NIC) og porter.

**Arbeidskø:** Opprett det private elevrepoet, åpne det i VS Code, skriv planen, undersøk klienten, oppdater komponentoversikten og registrer endringen med `git commit`.

**Dagens endring:** Du kan vise minst én dokumentert komponent i `arbeid/komponentoversikt.md` og den første registrerte Git-endringen.

**Neste steg:** I morgen følger du klientens fysiske forbindelse til nettverksutstyret.

**Fagstoff og verktøy:** [Datamaskinens komponenter – NDLA Vg1](https://ndla.no/e/teknologiforstaelse-im-ikm-vg1/datamaskinens-komponenter/dbd8bc410a) · [minnehierarki – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/minnehierarki/6fbc22ea30) · [Git i terminalen, GitHub Desktop og VS Code](../ressurser/git.md) · [VS Code og Markdown](../ressurser/programvare.md#vs-code-og-markdown)

## Tirsdag

**Dagens tema:** Ethernet og MAC-adresser. Du skal forstå hvordan klienten er fysisk koblet til det lokale nettverket.

**Dagens arbeid:** Følg kabelen eller den trådløse forbindelsen fra egen klient til nærmeste nettverksutstyr. Finn svitsj, ruter, aksesspunkt, Ethernet, RJ45, MAC-adresse og lokale fysiske forbindelser. Bruk deretter UniFi Network til å følge forbindelsen videre inn i den delte infrastrukturen.

**Arbeidskø:** Følg den fysiske forbindelsen, identifiser Flex Mini og Dream Router, kontroller klient og port i UniFi Network, og før funnene i komponentoversikten.

**Dagens endring:** Du kan vise hvilken enhet og port klienten er koblet til, og hvordan funnet ble kontrollert.

**Neste steg:** I morgen tegner du den fysiske forbindelsen og utvider den til hele IT-laben.

**Fagstoff og verktøy:** [Komponentene i datanettverk – NDLA Vg2](https://ndla.no/e/driftsstotte-im-itk-vg2/komponentene-i-datanettverk/6acd26e59c) · [5-lags TCP/IP-modell – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/5-lags-tcpip-modell/9e31c212f6) · [svitsj – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/svitsj/a33b4b015c) · [følg stasjonen i UniFi Network](../ressurser/unifi-network.md)

## Onsdag

**Dagens tema:** Fysisk topologi. Du skal forstå forskjellen mellom en komponentliste og et diagram over faktiske forbindelser.

**Dagens arbeid:** Se først hvordan én komponent og én fysisk forbindelse blir merket. Tegn deretter egen stasjon og utvid diagrammet med forbindelsen via svitsj og ruter og videre til de fysiske hovedkomponentene i hele IT-laben.

**Arbeidskø:** Åpne diagrammet, erstatt plassholderne med ID, modell og type, tegn klienten ved stasjonen, merk observerte grensesnitt og porter, utvid med felleskomponenter og eksporter en SVG-forhåndsvisning.

**Dagens endring:** Du kan vise en fysisk topologi med entydige komponent-ID-er og merkede forbindelser som begynner ved egen stasjon og følger observerte forbindelser videre.

**Neste steg:** I morgen undersøker du operativsystemet, maskinrollen og klientens nettverksverdier.

**Fagstoff og verktøy:** [Hva bør du dokumentere i IT-systemer – NDLA Vg1](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0) · [etiketter i topologidiagrammer](../ressurser/diagrametiketter.md#fysisk-topologi) · [diagrams.net](../ressurser/programvare.md#diagramsnet)

## Torsdag

**Dagens tema:** Operativsystem, klient og server. Du skal forstå forskjellen mellom maskinen, programvaren som styrer den, og rollen den har i systemet.

**Dagens arbeid:** Skill mellom fysisk maskin, operativsystem og rolle. Observer MAC-adresse, IP-adresse, subnett og standard gateway. Verdiene skal forstås før de brukes til feilsøking.

**Arbeidskø:** Finn riktig nettverkskort, les de aktuelle feltene i `ipconfig /all`, før verdiene i komponentoversikten og forklar kort hva de brukes til.

**Dagens endring:** Du kan vise klientens dokumenterte MAC-adresse, IP-adresse, subnett og standard gateway uten hemmeligheter eller unødvendige identifikatorer.

**Neste steg:** I morgen kontrollerer og forbedrer du ukens arbeid før det sendes til GitHub.

**Fagstoff og verktøy:** [Operativsystem – NDLA Vg1](https://ndla.no/nb/r/teknologiforstaelse-im-ikm-vg1/operativsystem/c04d611412) · [klargjøre maskin til å brukes som server – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/klargjore-maskin-til-a-brukes-som-server/14e705c5ae) · [IP, subnett og standard gateway](../ressurser/ip-og-subnett.md) · [`ipconfig /all`](../ressurser/nettverkskommandoer.md#finn-nettverkskonfigurasjonen)

## Fredag

**Dagens tema:** Ukeskontroll og forbedring. Du skal vurdere om dokumentasjonen kan kontrolleres og forstås av en annen elev.

**Dagens arbeid:** Kontroller dokumentasjonen fra egen stasjon og videre gjennom det du hittil har kartlagt av IT-laben. Rett én mangel, registrer endringen og send den til GitHub med `git push`.

**Arbeidskø:** Gå gjennom ukeskontrollen, åpne arbeidsfilene fra `README.md`, sammenlign diagram og komponentoversikt, rett én mangel, registrer endringen og send den til GitHub.

**Dagens endring:** Du kan vise hva du forbedret, den registrerte Git-endringen og at den finnes i elevrepoet på GitHub.

**Neste steg:** I steg 2 skiller du nettverkskonfigurasjon fra kommunikasjon fram til en avtalt tjeneste.

**Verktøy:** [Git i terminalen, GitHub Desktop og VS Code](../ressurser/git.md)

## Verktøyprogresjon

Før du bruker kommandoer, skal du kunne skille fil fra mappe, åpne en terminal, kjenne igjen ledeteksten, skrive en kommando, skille resultat fra feilmelding og kopiere et relevant utdrag. Du skal også kunne skille en adresse fra et vertsnavn.

| Faglig spørsmål                                                         | Verktøy                     | Avgrenset elevhandling                                                                                                         | Kontrollpunkt                                                                                         |
| ----------------------------------------------------------------------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
| Hvordan lager du dokumentasjon som en annen elev kan åpne og forstå? | VS Code og Markdown         | Åpne riktig mappe, redigere `arbeid/komponentoversikt.md`, skrive en overskrift, lagre og følge en relativ lenke fra `README.md`. | Filene ligger riktig, kan åpnes fra `README.md` og viser hva som er dokumentert.                      |
| Hvordan viser du fysiske forbindelser presist?                          | diagrams.net                | Opprette figurer, bruke samme ID som i komponentoversikten og merke forbindelser med grensesnitt og port. Lagre som `arbeid/arkitektur/diagrammer/fysisk-topologi.drawio`. | Diagrammet kan åpnes igjen, alle plassholdere er erstattet, og forbindelsene stemmer med det observerte systemet. |
| Hvilken enhet og port er klienten koblet til?                           | [UniFi Network](../ressurser/unifi-network.md) | Følge klienten til Flex Mini, Dream Router og det aktuelle nettet uten å endre konfigurasjonen. | Funnet brukes som kontroll av den fysiske topologien og merkes som observert systeminformasjon. |
| Hvordan gjør du endringer sporbare?                                     | [Git i terminalen](../ressurser/git.md) | Bruke `git status` og `git diff`, velge en fil med `git add`, kontrollere med `git diff --staged` og registrere med `git commit`. | Du finner igjen endringen i historikken og kan forklare hva den registrerte endringen inneholder. |
| Hvordan finner du klientens observerbare nettverksverdier?              | Terminal og `ipconfig /all` | Åpne terminal, kjøre kommandoen og finne MAC-adresse, IP-adresse, subnett og standard gateway.                                 | Verdiene føres i dokumentasjonen uten hemmeligheter eller unødvendige identifikatorer.                |

## Ukeskontroll

Kontroller: Hva skulle være gjort? Hva er gjort? Kan du vise det? Fungerer det? Er det dokumentert? Hva må forbedres? Hva er neste steg?

- [ ] `arbeid/komponentoversikt.md` starter med egen stasjon og er utvidet med relevante felleskomponenter i IT-laben.
- [ ] `arbeid/arkitektur/diagrammer/fysisk-topologi.drawio` følger faktiske forbindelser fra egen stasjon og videre gjennom IT-laben.
- [ ] Komponentene har samme ID som i komponentoversikten, og kjente grensesnitt og porter er merket.
- [ ] MAC-adresse, IP-adresse, subnett og standard gateway er funnet og kort forklart.
- [ ] Jeg kan skille MAC-adresse fra IP-adresse og forklare hva Ethernet gjør i det lokale nettet.
- [ ] Delen `Min systemdokumentasjon` i `README.md` har en kort systembeskrivelse og et godkjent navn på startpunktet.
- [ ] Delen `Min arbeidsprosess` i systemoversikten har en plan for undersøkelsen.
- [ ] Git-historikken viser små, forklarte endringer.
- [ ] Jeg kan skille filinnhold, lagret fil og registrert Git-endring.
- [ ] Ukens endringer er sendt til GitHub og kan åpnes der.

## Hvis du blir tidlig ferdig

Kontroller én komponent mot en ny observasjon eller kilde. Forbedre rollen, relasjonen eller merknaden i komponentoversikten, og oppdater diagrammet dersom funnet endrer den fysiske forbindelsen.

**Neste steg:** Bruke nettverksmodellene til å undersøke nettverkskonfigurasjon og kommunikasjon fram til en tjeneste med veiledning.
