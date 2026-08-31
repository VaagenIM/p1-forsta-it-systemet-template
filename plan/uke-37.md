# Uke 37 – fra Ethernet til tjeneste

**Dato:** 7.–11. september 2026  
**Periodeplan:** [P1 – forstå IT-systemet](periodeplan.md)  
**Startside:** [Forstå IT-systemet](../README.md)
**Dager:** [Mandag](#mandag) · [tirsdag](#tirsdag) · [onsdag](#onsdag) · [torsdag](#torsdag) · [fredag](#fredag)

**Ukemål:** Følge hele nettverkskjeden og bruke den i en veiledet feilsøking av et avgrenset problem.

**Ressurser:** [NDLA-fagstoff for perioden](../ressurser/ndla-fagstoff.md) · [Programvare og verktøy](../ressurser/programvare.md) · [Nettverkskjeden](../ressurser/nettverkskjeden.md) · [Feilsøkingsmetoden](../ressurser/feilsoking.md)

**Muntlig gjennomgang:** Du får de godkjente testmålene, tjenesten du skal følge, nødvendig informasjon om nett og VLAN og det avgrensede feilscenarioet.

**Før du begynner:** Kontroller at ukens endringer fra uke 36 finnes på GitHub, og at du kan åpne terminalen på den avtalte klienten.

## Mandag

**Dagens tema:** Ethernet, MAC og ARP. Du skal forstå hvordan klienten finner MAC-adressen som hører til en lokal IP-adresse.

**Dagens arbeid:** Bruk klienten ved egen stasjon til å følge lokal kommunikasjon fra Ethernet og MAC-adresser til ARP, som kobler en lokal IP-adresse til en MAC-adresse.

**Arbeidskø:** Finn klientens MAC-adresse, bruk et godkjent lokalt mål, les den aktuelle raden i `arp -a`, og knytt observasjonen til riktig komponent og forbindelse.

**Dagens endring:** Du kan vise én kontrollert kobling mellom lokal IP-adresse og MAC-adresse og forklare hva ARP-observasjonen betyr.

**Neste steg:** I morgen bruker du IP-adresse og prefiks til å avgjøre om et mål er lokalt.

**Fagstoff og verktøy:** [5-lags TCP/IP-modell – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/5-lags-tcpip-modell/9e31c212f6) · [svitsj – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/svitsj/a33b4b015c) · [`arp -a`](../ressurser/nettverkskommandoer.md#se-lokale-ip--og-mac-koblinger)

## Tirsdag

**Dagens tema:** IP, subnett og standard gateway. Du skal forstå når klienten kan sende lokalt, og når trafikken må gå via en ruter.

**Dagens arbeid:** Finn ut om målet er lokalt eller ligger i et annet nett, og forklar når klienten trenger standard gateway.

**Arbeidskø:** Finn klientens IP-adresse og prefiks, sammenlign dem med et avtalt mål, avgjør om målet er lokalt, og kontroller hvilken standard gateway klienten bruker.

**Dagens endring:** Du kan vise én adressevurdering og forklare hvorfor trafikken går lokalt eller via standard gateway.

**Neste steg:** I morgen undersøker du hvordan DHCP og DNS støtter klientens kommunikasjon.

**Fagstoff og verktøy:** [IP-adresser – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/ip-adresser/3082395965) · [ruter – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/ruter/eb2ce6553f) · [IP, subnett og standard gateway](../ressurser/ip-og-subnett.md) · [nettverkskommandoer](../ressurser/nettverkskommandoer.md)

## Onsdag

**Dagens tema:** DHCP og DNS. Du skal forstå hvordan klienten får nettverksverdier og hvordan navn blir slått opp til IP-adresser.

**Dagens arbeid:** Undersøk hvordan klienten ved egen stasjon fikk nettverkskonfigurasjonen, hvor de delte tjenestene befinner seg, og hvordan et navn blir slått opp til en IP-adresse.

**Arbeidskø:** Finn DHCP- og DNS-server i `ipconfig /all`, slå opp et avtalt navn med `nslookup`, og knytt serverne og resultatet til komponentoversikten.

**Dagens endring:** Du kan vise hvor klientens nettverksverdier kom fra, og hvilken IP-adresse et avtalt navn ble slått opp til.

**Neste steg:** I morgen følger du hele forbindelsen fram til tjenesten og tegner den logiske topologien.

**Fagstoff og verktøy:** [DHCP – NDLA Vg2](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dhcp/8755440e02) · [DNS-oppslag – NDLA Vg2](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dns-oppslag/8b81c28535) · [`ipconfig /all` og `nslookup`](../ressurser/nettverkskommandoer.md#windows-klient)

## Torsdag

**Dagens tema:** Tjeneste og logisk topologi. Du skal forstå hvordan nett, gateway, DNS og tjeneste henger sammen uten å blande dem med fysisk kabling.

**Dagens arbeid:** Se først hvordan ett nettverk, én standard gateway og én tjeneste blir merket. Følg deretter forbindelsen fra egen stasjon fram til en avtalt tjeneste. Tegn nett, gateway, DHCP, DNS og tjeneste i sammenheng med resten av IT-laben. Identifiser VLAN som logisk segmentering uten å endre konfigurasjonen.

**Arbeidskø:** Gjennomfør den avtalte tjenestetesten, finn aktuelt nett eller VLAN, erstatt plassholderne med bekreftede navn og verdier, tegn DHCP og DNS som egne tjenester, merk relasjonene og kontroller mot komponentoversikten.

**Dagens endring:** Du kan vise en logisk forbindelse med navngitte nettverk, tjenester og relasjoner fra klienten ved stasjonen til en avtalt tjeneste.

**Neste steg:** I morgen bruker du kjeden til å løse og dokumentere et kontrollert problem.

**Fagstoff og verktøy:** [Nettverkstjenester og protokoller – NDLA Vg2](https://ndla.no/e/driftsstotte-im-itk-vg2/nettverkstjenester-og-protokoller/d4b104e3ab) · [virtuelt lokalnettverk (VLAN) – NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelt-lokalnettverk-vlan/9d865afa88) · [etiketter i topologidiagrammer](../ressurser/diagrametiketter.md#logisk-topologi) · [test en tjeneste](../ressurser/tjenestetest.md) · [diagrams.net](../ressurser/programvare.md#diagramsnet) · [UniFi Network](../ressurser/unifi-network.md)

## Fredag

**Dagens tema:** Veiledet feilsøking. Du skal forstå hvordan én observasjon brukes til å velge neste relevante test.

**Dagens arbeid:** Se først en demonstrasjon av én feilsøking. Løs deretter et avgrenset problem med støtte. Dokumenter hva som oppsto, hvordan det ble løst og hvordan du kontrollerte løsningen.

**Arbeidskø:** Observer problemet, formuler en hypotese, velg én test, vurder resultatet, gjennomfør avtalt løsning og kontroller at problemet er borte.

**Dagens endring:** Du kan vise et dokumentert problem med årsak, løsning og kontroll i `arbeid/feilsoking.md`.

**Neste steg:** I uke 38 bruker du arbeidsmåten mer selvstendig og kobler tjenesten til virtuell og fysisk infrastruktur.

**Fagstoff og verktøy:** [Feilsøking på nettverk og maskin – NDLA Vg1](https://ndla.no/nb/r/teknologiforstaelse-im-ikm-vg1/feilsoking-pa-nettverk-og-maskin/c1b1b6defb) · [feilsøkingsmetodikk – NDLA Vg1](https://ndla.no/r/teknologiforstaelse-im-ikm-vg1/feilsokingsmetodikk/ad89a52950) · [nettverkskommandoer](../ressurser/nettverkskommandoer.md) · [tjenestetest](../ressurser/tjenestetest.md)

## Verktøyprogresjon

| Faglig spørsmål | Verktøy | Avgrenset elevhandling | Kontrollpunkt |
|---|---|---|---|
| Hvordan finner klienten en lokal MAC-adresse? | `arp -a` | Finne en avtalt lokal IP-adresse og tilhørende MAC-adresse i ARP-tabellen. | Du forklarer koblingen mellom IP-adresse og MAC-adresse som en observasjon. |
| Hvordan fikk klienten nettverkskonfigurasjonen sin? | `ipconfig /all` | Finne DHCP-server, DNS-server, IP-adresse, subnett og standard gateway og knytte verdiene til riktig funksjon. | Du peker ut relevante felt og forklarer hva de brukes til. |
| Hvordan blir et navn til en IP-adresse? | `nslookup` | Slå opp et avtalt navn, lese svaret og sammenligne navn og adresse. | Resultatet føres som observasjon, ikke som antakelse. |
| Hvor stopper kommunikasjonen? | `ping` og en avtalt tjenestetest | Teste fra lokal forbindelse via standard gateway og navneoppslag fram til tjenesten. | Du velger neste test ut fra forrige resultat. |
| Hvordan viser du fysisk og logisk nettverk uten å blande dem? | diagrams.net | Videreutvikle `arbeid/arkitektur/diagrammer/logisk-topologi.drawio` med funksjonelt nettnavn, VLAN, nett/prefiks, gateway, separate tjenester og navngitte relasjoner. | Diagrammet skiller fysisk forbindelse fra logisk tilhørighet og bruker samme ID-er som resten av dokumentasjonen. |
| Hvordan dokumenterer du et problem og løsningen? | VS Code, Markdown og [Git](../ressurser/git.md) | Beskrive hva som oppsto, hva som ble prøvd, årsaken, løsningen og kontrollen i `arbeid/feilsoking.md`. Bruk terminalkommandoene med mindre veiledning; bruk gjerne GitHub Desktop eller VS Code til å se forskjellen. | Arbeidsfil og Git-historikk viser hva som ble løst og hvordan. |

## Ukeskontroll

Kontroller: Hva skulle være gjort? Hva er gjort? Kan du vise det? Fungerer det? Er det dokumentert? Hva må forbedres? Hva er neste steg?

- [ ] Jeg kan forklare hvert ledd i Ethernet/MAC -> ARP -> IP/subnett -> standard gateway -> DHCP -> DNS -> tjeneste.
- [ ] `arbeid/arkitektur/diagrammer/logisk-topologi.drawio` følger forbindelsen fra egen stasjon til de delte nettverkene og tjenestene i IT-laben.
- [ ] Nettverk, gateway, DHCP, DNS og avtalt tjeneste har korrekte etiketter etter diagramstandarden.
- [ ] Avhengigheter til ARP, DHCP, DNS, standard gateway og tjeneste er forklart med observerte verdier.
- [ ] `arbeid/feilsoking.md` beskriver hva som oppsto, årsaken, løsningen og kontrollen.
- [ ] Hemmeligheter, personopplysninger og unødvendige identifikatorer er utelatt.
- [ ] Jeg kan velge neste nettverkstest ut fra forrige resultat med støtte.
- [ ] Ukens endringer er registrert og sendt til GitHub.

## Hvis du blir tidlig ferdig

Velg én forbindelse i den logiske topologien. Forklar skriftlig hvilke ledd som må virke for at klienten skal nå tjenesten, og lenk forklaringen til riktig diagram eller komponent.

**Neste steg:** Feilsøke et kontrollert problem mer selvstendig og følge en tjeneste gjennom virtuell og fysisk infrastruktur.
