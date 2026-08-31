# Uke 38 – virtualisering og systemhelhet

**Dato:** 14.–18. september 2026  
**Periodeplan:** [P1 – forstå IT-systemet](periodeplan.md)  
**Startside:** [Forstå IT-systemet](../README.md)
**Dager:** [Mandag](#mandag) · [tirsdag](#tirsdag) · [onsdag](#onsdag) · [torsdag](#torsdag) · [fredag](#fredag)

**Ukemål:** Bruke nettverkskjeden i kontrollert feilsøking, skille fysisk fra virtuell infrastruktur og forklare systemet som en sammenhengende arkitektur.

**Ressurser:** [NDLA-fagstoff for perioden](../ressurser/ndla-fagstoff.md) · [Nettverkskommandoer](../ressurser/nettverkskommandoer.md) · [Proxmox VE](../ressurser/proxmox-ve.md) · [Linux-konsoll](../ressurser/linux-konsoll.md) · [Feilsøkingsmetoden](../ressurser/feilsoking.md)

**Muntlig gjennomgang:** Du får vite hvilken Proxmox-node, virtuell maskin og tjeneste du skal undersøke, hvordan du får lesetilgang, og hvilke opplysninger du kan dokumentere.

**Før du begynner:** Kontroller at du kan åpne Proxmox VE med lesetilgang, og at fysisk og logisk topologi fra uke 36–37 er tilgjengelig.

## Mandag

**Dagens tema:** Selvstendig, kontrollert feilsøking. Du skal bruke nettverkskjeden til å velge test uten en ferdig oppskrift.

**Dagens arbeid:** Bruk Ethernet/MAC -> ARP -> IP/subnett -> standard gateway -> DHCP -> DNS -> tjeneste til å avgrense et avtalt problem. Dokumenter hva som oppsto, hvordan det ble løst og hvordan løsningen ble kontrollert.

**Arbeidskø:** Beskriv problemet, velg startpunkt i kjeden, test én hypotese om gangen, gjennomfør avtalt løsning, og kontroller samme funksjon på nytt.

**Dagens endring:** Du kan vise hvorfor du valgte testene, hva årsaken var, og hvordan du kontrollerte løsningen.

**Neste steg:** I morgen undersøker du hvordan virtuelle ressurser bygger på en fysisk vert.

**Fagstoff og verktøy:** [Feilsøkingsmetodikk – NDLA Vg1](https://ndla.no/r/teknologiforstaelse-im-ikm-vg1/feilsokingsmetodikk/ad89a52950) · [feilsøking på nettverk og maskin – NDLA Vg1](https://ndla.no/nb/r/teknologiforstaelse-im-ikm-vg1/feilsoking-pa-nettverk-og-maskin/c1b1b6defb) · [nettverkskommandoer](../ressurser/nettverkskommandoer.md) · [tjenestetest](../ressurser/tjenestetest.md)

## Tirsdag

**Dagens tema:** Virtualisering. Du skal forstå forholdet mellom fysisk vert, hypervisor, virtuell maskin og container.

**Dagens arbeid:** Undersøk hva som skjer når maskinressurser blir gjort tilgjengelige som virtuelle ressurser.

**Arbeidskø:** Les om virtuelle maskiner, sammenlign fysisk og virtuell maskin, finn hvilke ressurser en gjest trenger, og tegn en enkel avhengighet fra gjest til vert.

**Dagens endring:** Du kan vise en kort forklaring eller skisse som skiller vertsmaskin, hypervisor og gjest.

**Neste steg:** I morgen finner du de samme delene i Proxmox VE og kobler dem til nettverket.

**Fagstoff:** [Virtuelle maskiner – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelle-maskiner/b8a976125b)

## Onsdag

**Dagens tema:** Proxmox VE og virtuelle ressurser. Du skal forstå hvor en tjeneste kjører, og hvordan gjesten er koblet til verten og nettverket.

**Dagens arbeid:** Finn de avtalte ressursene i IT-laben: fysisk server -> hypervisor -> virtuelle maskiner eller containere. Koble dem til nettverket og tjenestene du allerede har fulgt fra egen stasjon.

**Arbeidskø:** Finn avtalt node, VM eller container, tildelte ressurser, virtuelt nettverkskort og Linux-bro. Bruk riktig konsoll hvis oppgaven krever Linux-kommandoer.

**Dagens endring:** Du kan vise relasjonen mellom tjeneste, gjest, Proxmox-node, Linux-bro og fysisk nettverk uten å endre konfigurasjonen.

**Neste steg:** I morgen samler du den fysiske, logiske og virtuelle modellen i én systemforklaring.

**Fagstoff og verktøy:** [Virtuelle maskiner – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelle-maskiner/b8a976125b) · [Proxmox VE](../ressurser/proxmox-ve.md) · [Linux-konsoll i Proxmox](../ressurser/linux-konsoll.md)

## Torsdag

**Dagens tema:** Avhengigheter og systemarkitektur. Du skal forstå hvordan flere dokumenterte deler blir én sammenhengende modell.

**Dagens arbeid:** Bygg sammen den fysiske, logiske og virtuelle modellen. Finn hva som er avhengig av hva.

**Arbeidskø:** Sammenlign komponentoversikten og begge diagrammene, velg én tjeneste, følg den gjennom alle lagene, og oppdater systemoversikten med lenker til beleggene.

**Dagens endring:** Du kan vise en sammenhengende og kontrollert avhengighetskjede i systemoversikten.

**Neste steg:** I morgen bruker du dokumentasjonen til å forklare systemet og forbedrer den etter tilbakemelding.

Eksempel:

> Webtjeneste -> virtuell maskin (VM) -> Proxmox VE -> fysisk server -> svitsj -> ruter

**Fagstoff og verktøy:** [Hva bør du dokumentere i IT-systemer – NDLA Vg1](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0) · [diagrams.net](../ressurser/programvare.md#diagramsnet)

## Fredag

**Dagens tema:** Forklar systemet. Du skal vise at en annen elev kan navigere i dokumentasjonen og følge sammenhengene.

**Dagens arbeid:** Bruk egen stasjon som startpunkt i en kort gjennomgang for en annen elev. Forklar derfra hele IT-laben: fysisk og logisk topologi, tjenester, servere og virtuelle ressurser.

**Arbeidskø:** Gjennomfør fagfellekontrollen, velg én forbedring, oppdater dokumentasjonen, eksporter diagrammene som SVG, registrer siste endring og send den til GitHub.

**Dagens endring:** Du kan vise hva fagfellekontrollen avdekket, hvilken forbedring du gjorde, og et ferdig elevrepo på GitHub.

**Neste steg:** Lever det ferdige repoet som din individuelle systemforklaring, og ta med erfaringene videre til neste periode.

**Verktøy:** [VS Code og Markdown](../ressurser/programvare.md#vs-code-og-markdown) · [Git i terminalen, GitHub Desktop og VS Code](../ressurser/git.md)

### Fagfellekontroll

1. Åpne hverandres elevrepo på GitHub.
2. Følg lenkene fra `README.md` til systemoversikten og diagrammene.
3. Finn én sammenheng som er tydelig, og still ett konkret spørsmål om noe som mangler eller er uklart.
4. Skriv tilbakemeldingen kort.
5. Velg én forbedring, gjennomfør den og registrer endringen med `git commit`.

Hvis muntlig fagfellekontroll ikke passer, kan den samme kontrollen gjennomføres skriftlig.

## Verktøyprogresjon

| Faglig spørsmål | Verktøy | Avgrenset elevhandling | Kontrollpunkt |
|---|---|---|---|
| Hvor i nettverkskjeden ligger problemet? | [Windows- eller Linux-kommandoer](../ressurser/nettverkskommandoer.md) og [avtalt tjenestetest](../ressurser/tjenestetest.md) | Velge neste test ut fra forrige resultat, løse problemet og dokumentere løsningen i `arbeid/feilsoking.md`. | Dokumentasjonen viser hva som oppsto, årsaken, løsningen og kontrollen. |
| Hvor kjører den virtuelle ressursen? | [Proxmox VE](../ressurser/proxmox-ve.md) | Logge inn, skille node fra VM eller container og finne status og tildelte ressurser. | Du kan peke ut fysisk vert, virtuell ressurs og sentrale ressurser uten å endre konfigurasjonen. |
| Hvordan er den virtuelle ressursen koblet til nettverket? | Proxmox og nettverksdiagram | Finne relevant nettverkskobling og plassere den virtuelle ressursen i den fysiske og logiske modellen. | Samme navn og relasjoner brukes konsekvent i Proxmox-observasjon og diagram. |
| Hvilke belegg støtter systemforklaringen? | VS Code, Markdown og relative lenker | Koble `arbeid/arkitektur/oversikt.md` til komponentoversikt, diagrammer og dokumenterte problemer og løsninger. | En medelev kan følge lenkene og kontrollere forklaringen. |
| Hvordan viser historikken utviklingen fra observasjon til helhet? | [Git](../ressurser/git.md) | Kontrollere forskjeller og historikk i terminalen, GitHub Desktop eller VS Code, rette ett belegg etter fagfellekontroll og registrere en avsluttende endring. | Du kan vise hvilken tilbakemelding som førte til hvilken endring. |

## Sluttkontroll

Kontroller: Hva skulle være gjort? Hva er gjort? Kan du vise det? Fungerer det? Er det dokumentert? Hva må forbedres? Hva er neste steg?

- [ ] `arbeid/arkitektur/oversikt.md` forklarer hele IT-labens avgrensning, hovedkomponenter og avhengigheter med egen stasjon som startpunkt.
- [ ] Komponentoversikt, fysisk topologi og logisk topologi stemmer overens.
- [ ] Samme ID-er brukes overalt, alle viktige relasjoner er merket, og ingen plassholdere eller spørsmålstegn står igjen i diagrammene.
- [ ] Minst ett avgrenset problem er løst ved hjelp av nettverkskjeden og dokumentert i `arbeid/feilsoking.md`.
- [ ] En tjeneste kan følges fra klienten ved egen stasjon gjennom nettverket til VM, hypervisor og fysisk vert.
- [ ] En medelev har gitt tilbakemelding, og ett valgt belegg er forbedret.
- [ ] Repoet forklarer systemet med presis fagterminologi og konkrete belegg.
- [ ] Repoet kobler Proxmox-observasjoner, dokumentasjon og Git-historikk til samme systemforklaring.
- [ ] Diagrammene er eksportert som `.svg`, og siste endring er sendt til GitHub.

## Hvis du blir tidlig ferdig

Velg én avhengighet i systemoversikten. Forbedre forklaringen slik at en annen elev kan følge den fra tjenesten til den fysiske verten og tilbake til klienten.

**Neste steg:** Fordype virtualisering, tjenester, automatisering og gjenoppretting i P3.
