# Følg stasjonen i UniFi Network

Bruk denne siden for å kontrollere den fysiske og logiske nettverkstilkoblingen uten å endre UniFi-konfigurasjonen.

## Utstyret ved stasjonen

Hver stasjon er koblet til en **UniFi Flex Mini** og en **UniFi Dream Router**.

| Enhet | Rolle i undersøkelsen | Offisiell dokumentasjon |
|---|---|---|
| UniFi Flex Mini (`USW-Flex-Mini`) | administrert lag-2-svitsj med fem Ethernet-porter | [Flex Mini - tekniske spesifikasjoner](https://techspecs.ui.com/unifi/switching/usw-flex-mini?subcategory=switching-utility) |
| UniFi Dream Router (`UDR`) | gateway med UniFi Network, ruting, DHCP-mulighet, svitsjporter og trådløst nett | [Dream Router - tekniske spesifikasjoner](https://techspecs.ui.com/unifi/cloud-gateways/udr?subcategory=cloud-gateways-wifi-integrated) |

Den faktiske kablingen, portbruken, nettverket og eventuelle VLAN blir forklart i den muntlige gjennomgangen. Kontroller dette mot det du ser; ikke fyll inn manglende opplysninger ved å gjette.

> **Kort sagt:** Flex Mini kobler lokale Ethernet-enheter sammen. Dream Router kobler og styrer nettverkene ved stasjonen.

## Finn klienten og forbindelsen

1. Åpne klientoversikten i UniFi Network.
2. Finn den avtalte klienten ved hjelp av et godkjent navn eller en godkjent adresse.
3. Noter klientens IP-adresse, MAC-adresse og nett/VLAN når disse feltene er tilgjengelige.
4. Finn hvilken enhet og port klienten er koblet til.
5. Åpne enhetsoversikten og finn Flex Mini og Dream Router ved stasjonen.
6. Følg den observerte forbindelsen mellom klient, port, svitsj, gateway og det delte nettet.
7. Sammenlign funnet med den fysiske kablingen og topologidiagrammet.

Grensesnittet kan ha andre navn avhengig av UniFi-versjon og tilgangsnivå. Se etter funksjonene klienter, enheter, porter og nettverk.

Kilder: [Komponentene i datanettverk - NDLA Vg2](https://ndla.no/e/driftsstotte-im-itk-vg2/komponentene-i-datanettverk/6acd26e59c), [UniFi Switch Settings](https://help.ui.com/hc/en-us/articles/33402927617047-UniFi-Switch-Settings) og [Creating Virtual Networks (VLANs)](https://help.ui.com/hc/en-us/articles/9761080275607-Creating-Virtual-Networks-VLANs).

## Fysisk og logisk funn

| Funn | Hører hjemme i |
|---|---|
| kabel, enhet, svitsjport og uplink | fysisk topologi |
| IP-adresse, subnett, nett/VLAN og standard gateway | logisk topologi |
| enhetsnavn, modell og rolle | komponentoversikten |

En UniFi-visning er ett belegg. Kontroller den mot fysisk observasjon, klientens nettverksverdier og opplysninger fra den muntlige gjennomgangen.

## Ikke gjør endringer

Ikke endre porter, portprofiler, VLAN, nettverk, DHCP, DNS, trådløse innstillinger, brannmur eller enhetskonfigurasjon. Stopp hvis en handling viser `Apply`, `Save` eller en tilsvarende bekreftelse.
