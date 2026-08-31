# Periodeplan – forstå IT-systemet

**Periode:** Uke 36–38, 31. august–18. september 2026  
**Ukeplaner:** [Uke 36](uke-36.md) · [uke 37](uke-37.md) · [uke 38](uke-38.md)  
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
- en gjennomgang av repoet
- hvilke systemnavn og tekniske verdier du kan lagre i repoet

Ikke skriv inn passord eller andre innloggingsopplysninger. Hvis du mangler ett av punktene, skal du be om det før du undersøker den aktuelle delen av laben.

## Begreper

Du skal kunne bruke og forklare:

Åpne [NDLA-fagstoff for perioden](../ressurser/ndla-fagstoff.md) når du trenger en forklaring eller skal repetere et begrep.

- IT-system
- arkitektur
- komponent
- infrastruktur
- klient
- server
- tjeneste
- avhengighet
- operativsystem
- nettverkskort (network interface card, NIC)
- svitsj (switch)
- ruter (router)
- Ethernet
- MAC-adresse
- ARP
- IP-adresse
- subnettmaske eller prefiks
- standard gateway (default gateway)
- DHCP
- DNS
- VLAN
- virtuell maskin (virtual machine, VM)
- hypervisor
- repo (repository)
- versjonskontroll (version control)
- `git commit`
- komponentoversikt (system component inventory)
- fysisk og logisk topologi
- feilsøking

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
- følge og forklare nettverkskjeden fra Ethernet/MAC via ARP, IP/subnett, standard gateway, DHCP og DNS til en tjeneste
- skille mellom fysisk og virtuell infrastruktur
- dokumentere systemets arkitektur med komponentoversikt, topologidiagram og systemoversikt
- bruke Git til å registrere og følge endringer
- feilsøke med **observasjon -> hypotese -> test**
- forklare systemet til andre

**Målet er at du kan undersøke et IT-system og forklare hva det består av, hvordan det virker og hvordan det er dokumentert.**

## Faglig progresjon

Nettverksforståelsen bygges i denne rekkefølgen:

**Ethernet/MAC -> ARP -> IP/subnett -> standard gateway -> DHCP -> DNS -> tjeneste**

1. I uke 36 undersøker du fysisk forbindelse, Ethernet, MAC-adresse og klientens nettverksverdier.
2. I uke 37 følger du hele [nettverkskjeden](../ressurser/nettverkskjeden.md) med veiledning og dokumenterer ett avgrenset problem.
3. I uke 38 bruker du kjeden i en selvstendig, kontrollert feilsøking før du kobler tjenesten til virtuell og fysisk infrastruktur.


| Du skal kunne                                      | Slik gjør du det                                                                                                                                                                                                | Dette viser at du kan det                                    |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| **finne komponentene i et IT-system**              | Start ved egen stasjon og følg forbindelsene videre gjennom IT-laben. Finn klient, server, nettverkskort, svitsj, ruter og hypervisor.                                                                          | `arbeid/komponentoversikt.md`                                |
| **forklare hvilken rolle de har**                  | Undersøk én komponent om gangen. Beskriv hva den gjør og hvorfor systemet trenger den.                                                                                                                          | Komponentoversikt og korte forklaringer                      |
| **vise forbindelser og avhengigheter**             | Følg forbindelsene fra egen stasjon via den delte infrastrukturen til servere og tjenester. Tegn hele IT-laben.                                                                                                 | Fysisk og logisk topologi                                    |
| **forklare grunnleggende nettverkskommunikasjon**  | Følg kjeden Ethernet/MAC -> ARP -> IP/subnett -> standard gateway -> DHCP -> DNS -> tjeneste. Bruk [nettverkskommandoene](../ressurser/nettverkskommandoer.md) til å observere leddene fra Windows eller Linux. | Nettverkskart og forklaring                                  |
| **skille mellom fysisk og virtuell infrastruktur** | Følg [Proxmox-framgangsmåten](../ressurser/proxmox-ve.md), finn vertsmaskin og gjestemaskin og bruk [Linux-konsollen](../ressurser/linux-konsoll.md) på riktig system.                                          | Diagram og komponentoversikt                                 |
| **dokumentere systemet**                           | Oppdater delen `Min systemdokumentasjon` i `README.md`, registrer fakta i komponentoversikten, tegn diagrammene og bruk systemoversikten til å forklare helheten.                                               | `README.md`, systemoversikt, komponentoversikt og diagrammer |
| **bruke Git**                                      | Klon elevrepoet og lær først [arbeidsflyten i terminalen](../ressurser/git.md). Bruk deretter GitHub Desktop eller Git i VS Code gradvis som støtte.                                                           | Git-historikk                                                |
| **feilsøke systematisk**                           | Etter veiledet øving får du et avgrenset problem. Følg nettverkskjeden, test én relevant hypotese om gangen og dokumenter hva som oppsto og hvordan det ble løst.                                               | `arbeid/feilsoking.md`                                       |
| **forklare systemet til andre**                    | Bruk egen dokumentasjon og diagram til å forklare systemet for en medelev og forbedre uklare deler.                                                                                                             | Fagfellekontroll og forbedret repo                           |

## Slik vurderes arbeidet

Du får underveisvurdering gjennom veiledning, ukeskontroller og fagfellekontroll. Etter fristen får du en skriftlig sluttkommentar. Det ferdig leverte repoet er din individuelle systemforklaring.

Se [vurderingssiden](vurdering.md) for aktuelle kompetansemål fra ITK02-01, vurderingsbelegg og sluttkontroll.

## Leveranse

Du leverer elevrepoet gjennom Classroom50. Følg [leveringsstegene i `README.md`](../README.md#levering).
