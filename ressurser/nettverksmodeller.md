# Nettverksmodeller

Bruk tre ulike modeller. De svarer på ulike spørsmål og skal ikke blandes sammen.

## Nettverkskonfigurasjon

DHCP kan gi klienten nettverksverdiene den trenger:

```text
DHCP
├── IP-adresse og prefiks
├── standard gateway
└── DNS-server
```

DHCP er derfor en tjeneste som konfigurerer klienten. Den er ikke et ledd mellom gateway og DNS når klienten kommuniserer.

## Kommunikasjon fram til en tjeneste

Når klienten skal bruke en tjeneste, undersøker du disse delene etter behov:

```text
Ethernet og MAC-adresser
→ ARP i det lokale nettet
→ IP-adresse og prefiks
→ gateway og ruting når målet er i et annet nett
→ DNS når klienten bruker et navn
→ tjeneste, protokoll og port
```

| Del | NDLA-fagstoff | Spørsmål du skal kunne svare på | Aktuell observasjon eller kontroll |
|---|---|---|---|
| Ethernet og MAC-adresse | [5-lags TCP/IP-modell – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/5-lags-tcpip-modell/9e31c212f6) og [svitsj – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/svitsj/a33b4b015c) | Hvordan er klienten koblet til det lokale nettverket? | nettverkskort, kabel eller trådløs forbindelse, svitsjport og MAC-adresse |
| ARP | [5-lags TCP/IP-modell – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/5-lags-tcpip-modell/9e31c212f6) | Hvilken MAC-adresse hører til en lokal IP-adresse? | ARP-tabell med [Windows- eller Linux-kommando](nettverkskommandoer.md) |
| IP-adresse og prefiks | [IP-adresser – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/ip-adresser/3082395965) | Hvilken adresse har klienten, og er målet lokalt? | [IP-adresse, subnettmaske eller prefiks](ip-og-subnett.md) |
| Gateway og ruting | [Ruter – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/ruter/eb2ce6553f) | Hvor sendes trafikk som skal til et annet nettverk? | gateway-adresse og kontroll av forbindelse til gateway |
| DNS ved navnebruk | [DNS-oppslag – Vg2](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dns-oppslag/8b81c28535) | Hvordan blir et vertsnavn slått opp til en IP-adresse? | kontrollert navneoppslag med [aktuell kommando](nettverkskommandoer.md) |
| Tjeneste, protokoll og port | [Nettverkstjenester og protokoller – Vg2](https://ndla.no/e/driftsstotte-im-itk-vg2/nettverkstjenester-og-protokoller/d4b104e3ab) | Svarer tjenesten som brukeren trenger? | [avtalt tjenestetest](tjenestetest.md) |

## Feilsøkingsrekkefølge

Start med det grunnleggende og velg neste kontroll ut fra resultatet:

```text
fysisk forbindelse
→ nettverksgrensesnitt
→ IP-konfigurasjon
→ lokalt nett
→ gateway og ruting
→ DNS
→ tjeneste
```

Du er klar for veiledet feilsøking når du kan:

- forklare hva hvert kontrollpunkt undersøker
- finne relevante verdier uten å lagre hemmeligheter eller unødvendige identifikatorer
- skille en observasjon fra en antakelse
- velge neste kontroll ut fra resultatet fra forrige kontroll
