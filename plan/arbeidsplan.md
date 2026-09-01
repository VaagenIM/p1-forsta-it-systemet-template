# Periodeplan – forstå IT-systemet

**Arbeidssteg:** [Fysisk infrastruktur](steg-1-fysisk-infrastruktur.md) · [nettverk og tjenester](steg-2-nettverk-og-tjenester.md) · [virtualisering og systemhelhet](steg-3-virtualisering-og-systemhelhet.md)
**Vurdering:** [Kompetansemål, vurderingsbelegg og vurderingsform](vurdering.md)

I P1 skal du lære å finne ut hvordan et IT-system er bygget opp og hvordan delene henger sammen. Du skal også lære arbeidsmåter i IT-bransjen.

**Startside:** [Forstå IT-systemet](../README.md)

## Oppdrag

**Undersøk og dokumenter hele IT-laben slik at en annen IT-elev kan forstå hvordan den er bygget opp og begynne å arbeide med den.**

Start ved egen stasjon og følg forbindelsene utover:

```text
egen klient og kabling -> nærmeste nettverkstilkobling -> delt nettverksinfrastruktur
-> DHCP, DNS og andre tjenester -> servere, hypervisorer og virtuelle maskiner
```

Egen stasjon gir deg et konkret utgangspunkt for oppgaven. Dokumentasjonen skal likevel beskrive helheten i IT-laben, ikke bare utstyret ved stasjonen.

## Introduksjon og gjennomgang

Før de praktiske arbeidsstegene tar vi en gjennomgang av:

- hva som er forventet av deg og hvordan du kommer i mål
- hvilke deler av IT-laben som inngår i oppgaven
- en gjennomgang av elevrepoet
- hvilke systemnavn og tekniske verdier du kan lagre i elevrepoet

Ikke skriv inn passord eller andre innloggingsopplysninger. Hvis du mangler ett av punktene, skal du be om det før du undersøker den aktuelle delen av laben.

## Begreper

Begrepene introduseres når de trengs i arbeidsrekkefølgen. Åpne [NDLA-fagstoff for perioden](../ressurser/ndla-fagstoff.md) når dagens steg krever en forklaring eller repetisjon.

| Uke | Begreper du trenger i arbeidet |
|---|---|
| 36 | IT-system, komponent, infrastruktur, klient, server, operativsystem, nettverkskort (network interface card, NIC), svitsj (switch), ruter (router), Ethernet, MAC-adresse og fysisk topologi |
| 37 | ARP, IP-adresse, subnettmaske eller prefiks, standard gateway (default gateway), DHCP, DNS, VLAN, tjeneste, protokoll, feilsøking og logisk topologi |
| 38 | arkitektur, avhengighet, virtuell maskin (virtual machine, VM), hypervisor, kodearkiv (repository), versjonskontroll (version control) og `git commit` |

### Arkitektur, infrastruktur og topologi

| Begrep            | Betydning i denne perioden                                                                                                  | Arbeidsprodukt                                                                                                                                                            |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Arkitektur**    | Helheten: komponenter, roller, forbindelser og avhengigheter i IT-systemet.                                                 | [Systemoversikten](../arbeid/arkitektur/oversikt.md) samler forklaringen.                                                                                                 |
| **Infrastruktur** | Det tekniske grunnlaget: klienter, servere, nettverksutstyr, kabling, operativsystemer, hypervisorer og virtuelle maskiner. | Komponentoversikten og systemoversikten beskriver infrastrukturen.                                                                                                        |
| **Topologi**      | Hvordan komponentene er plassert og koblet sammen fysisk eller logisk.                                                      | Diagrammene viser [fysisk topologi](../arbeid/arkitektur/diagrammer/fysisk-topologi.drawio) og [logisk topologi](../arbeid/arkitektur/diagrammer/logisk-topologi.drawio). |

## Du skal kunne

- finne komponentene i hele IT-laben med utgangspunkt i egen stasjon
- forklare hvilken rolle de har
- vise forbindelser og avhengigheter
- forklare hvordan DHCP gir klienten nettverkskonfigurasjon, og hvordan kommunikasjon går via lokale nett, ruting og navneoppslag fram til en tjeneste
- skille mellom fysisk og virtuell infrastruktur
- dokumentere systemets arkitektur med komponentoversikt, topologidiagram og systemoversikt
- bruke Git til å registrere og følge endringer
- feilsøke med **observasjon -> hypotese -> test**
- forklare systemet til andre

**Målet er at du kan undersøke et IT-system og forklare hva det består av, hvordan det virker og hvordan det er dokumentert.**

## Faglig progresjon

Nettverksforståelsen bygges med tre modeller:

- **Nettverkskonfigurasjon:** DHCP gir klienten IP-adresse, prefiks, standard gateway og DNS-server.
- **Kommunikasjon:** Ethernet og MAC-adresser → ARP i det lokale nettet → IP-adresse og prefiks → gateway og ruting → DNS ved navnebruk → tjeneste, protokoll og port.
- **Feilsøking:** fysisk forbindelse → nettverksgrensesnitt → IP-konfigurasjon → lokalt nett → gateway og ruting → DNS → tjeneste.

1. I steg 1 undersøker du fysisk forbindelse, Ethernet, MAC-adresse og klientens nettverksverdier.
2. I steg 2 bruker du [nettverksmodellene](../ressurser/nettverksmodeller.md) med veiledning og dokumenterer ett avgrenset problem.
3. I steg 3 bruker du feilsøkingsrekkefølgen i en selvstendig, kontrollert feilsøking før du kobler tjenesten til virtuell og fysisk infrastruktur.


| Du skal kunne                                      | Slik gjør du det                                                                                                                                                                                                | Dette viser at du kan det                                    |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| **finne komponentene i et IT-system**              | Start ved egen stasjon og følg forbindelsene videre gjennom IT-laben. Finn klient, server, nettverkskort, svitsj, ruter og hypervisor.                                                                          | `arbeid/komponentoversikt.md`                                |
| **forklare hvilken rolle de har**                  | Undersøk én komponent om gangen. Beskriv hva den gjør og hvorfor systemet trenger den.                                                                                                                          | Komponentoversikt og korte forklaringer                      |
| **vise forbindelser og avhengigheter**             | Følg forbindelsene fra egen stasjon via den delte infrastrukturen til servere og tjenester. Tegn hele IT-laben.                                                                                                 | Fysisk og logisk topologi                                    |
| **forklare grunnleggende nettverkskommunikasjon**  | Skill mellom hvordan DHCP konfigurerer klienten, og hvordan kommunikasjon går gjennom relevante nettverksledd fram til en tjeneste. Bruk [nettverksmodellene](../ressurser/nettverksmodeller.md) og [nettverkskommandoene](../ressurser/nettverkskommandoer.md). | Nettverkskart og forklaring                                  |
| **skille mellom fysisk og virtuell infrastruktur** | Følg [Proxmox-framgangsmåten](../ressurser/proxmox-ve.md), finn vertsmaskin og gjestemaskin og bruk [Linux-konsollen](../ressurser/linux-konsoll.md) på riktig system.                                          | Diagram og komponentoversikt                                 |
| **dokumentere systemet**                           | Oppdater delen `Min systemdokumentasjon` i `README.md`, registrer fakta i komponentoversikten, tegn diagrammene og bruk systemoversikten til å forklare helheten.                                               | `README.md`, systemoversikt, komponentoversikt og diagrammer |
| **bruke Git**                                      | Klon elevrepoet og lær først [arbeidsflyten i terminalen](../ressurser/git.md). Bruk deretter GitHub Desktop eller Git i VS Code gradvis som støtte.                                                           | Git-historikk                                                |
| **feilsøke systematisk**                           | Etter veiledet øving får du et avgrenset problem. Bruk feilsøkingsrekkefølgen, test én relevant hypotese om gangen og dokumenter hva som oppsto og hvordan det ble løst.                                      | `arbeid/feilsoking.md`                                       |
| **forklare systemet til andre**                    | Bruk egen dokumentasjon og diagram til å forklare systemet for en medelev og forbedre uklare deler.                                                                                                             | Fagfellekontroll og forbedret elevrepo                       |

## Slik vurderes arbeidet

Du får underveisvurdering gjennom veiledning, ukeskontroller og fagfellekontroll. Etter fristen får du en skriftlig sluttkommentar. Det ferdig leverte elevrepoet er din individuelle systemforklaring.

Se [vurderingssiden](vurdering.md) for aktuelle kompetansemål fra ITK02-01, vurderingsbelegg og sluttkontroll.

## Leveranse

Du leverer elevrepoet gjennom Classroom50. Følg [leveringsstegene i `README.md`](../README.md#levering).
