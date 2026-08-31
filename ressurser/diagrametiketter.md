# Etiketter i topologidiagrammer

Et diagram skal kunne forstås uten at du står ved siden av og forklarer det. Bruk samme navn og ID i diagrammene, [komponentoversikten](../arbeid/komponentoversikt.md) og [systemoversikten](../arbeid/arkitektur/oversikt.md).

## Grunnregler

1. Gi diagrammet en tittel som viser om det er fysisk eller logisk topologi.
2. Gi hvert element et entydig navn eller en ID og vis hva slags element det er.
3. Merk forbindelser med det som gjør relasjonen forståelig, for eksempel porter, protokoll eller handling.
4. Bruk samme betegnelse for samme element overalt.
5. Bruk bare tekniske verdier som er observert, bekreftet eller oppgitt i den muntlige gjennomgangen.
6. Erstatt alle plassholdere som `<...>` og alle spørsmålstegn før levering.
7. Legg inn en kort tegnforklaring hvis farge, linjetype eller symbol har en egen betydning.

NDLA anbefaler at et nettverkskart viser de viktigste enhetene og hvordan de er koblet sammen. Kabler, koblingspunkter og uttak bør ha unike ID-er som også brukes i dokumentasjonen. Servere bør beskrives med navn og funksjon, mens nettverksdokumentasjonen bør vise relevante opplysninger som IP-adresser, VLAN, DNS og DHCP. Bruk reglene nedenfor slik at disse opplysningene vises på samme måte i alle diagrammene.

## Fysisk topologi

Den fysiske topologien viser faktiske enheter, tilkoblingspunkter og forbindelser. En komponentetikett bygges slik:

```text
<navn eller ID>
<modell når den er relevant>
<type eller fysisk rolle>
```

Eksempler:

```text
PC-01
Eksempelmodell 1000
klient
```

```text
SW-01
Mikrotik CRS305-1G-4S
svitsj
```

```text
RTR-01
TP-Link Omada
ruter
```

```text
PVE-01
Eksempelmodell 1000
virtualiseringsvert/ hypervisor
```

Merk en forbindelse med grensesnitt og port når disse er kjent:

```text
Ethernet: PC-01 Ethernet til SW-01 port 3
```

Bruk en heltrukken linje uten pil for en fysisk kabel eller Ethernet-forbindelse. Linjen viser tilkobling, ikke retning på trafikken.

Ikke skriv `standard gateway` som en del av den fysiske ruterens navn. **Ruter** er komponenttypen. **Standard gateway** er en logisk rolle og en IP-adresse på et rutergrensesnitt.

## Logisk topologi

Den logiske topologien viser nettverk, adresser, logiske roller, tjenester og avhengigheter.

Et nettverk merkes slik:

```text
<funksjonelt nettnavn>
VLAN <ID>
<nettadresse/prefiks>
```

En standard gateway merkes slik:

```text
Standard gateway
<IP-adresse>
<ruter-ID>
```

En tjeneste merkes slik:

```text
<tjenestenavn>
<vertsnavn eller komponent-ID>
<protokoll/port når relevant>
```

Eksempler:

```text
DNS-tjeneste
DNS-01
UDP/TCP 53
```

```text
Webtjeneste
WEB-01
HTTPS/443
```

DHCP og DNS skal stå som egne tjenester, selv om de kjører på samme komponent. Da blir det tydelig hvilken funksjon og avhengighet hver boks viser.

## Etiketter på relasjoner

Bruk et verb eller en presis teknisk beskrivelse som forklarer relasjonen:

- `bruker som standard gateway`
- `ruter trafikk til`
- `klienter får nettverksinnstillinger fra`
- `klienter slår opp navn hos`
- `kobler til med HTTPS/443`
- `kjører på`

Unngå utydelige etiketter som bare `bruker`, `kobling` eller `til`.

Bruk pil i den logiske topologien når retningen har betydning. Pilretningen og teksten skal uttrykke den samme relasjonen.

## Kontroll før eksport

- [ ] Diagrammet har riktig tittel og viser bare én tydelig visning.
- [ ] Alle komponenter, nettverk og tjenester har navn eller ID.
- [ ] Type, rolle og teknisk verdi er ikke blandet sammen.
- [ ] DHCP og DNS er tegnet som separate tjenester.
- [ ] Viktige forbindelser og piler har forklarende etiketter.
- [ ] Samme ID brukes i begge diagrammer og i komponentoversikten.
- [ ] Ingen `<...>`, `?` eller generiske startnavn står igjen.
- [ ] En annen elev kan forstå diagrammet uten ekstra forklaring.

Kilde: [Hva bør du dokumentere i IT-systemer? – NDLA](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0). Videre lesning: [ISO/IEC/IEEE 42010:2022](https://www.iso.org/standard/74393.html) og [C4-modellens anbefalinger for diagramnotasjon](https://c4model.com/diagrams/notation).
