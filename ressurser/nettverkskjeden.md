# Nettverkskjeden

Før du feilsøker selvstendig, skal du kunne følge denne rekkefølgen:

```text
Ethernet/MAC - ARP - IP/subnett - standard gateway - DHCP - DNS - tjeneste
```

Rekkefølgen er en modell for å forstå og undersøke nettverket. Den er ikke en påstand om at protokollene alltid brukes i akkurat denne tidsrekkefølgen.

| Ledd | NDLA-fagstoff | Spørsmål du skal kunne svare på | Aktuell observasjon eller kontroll |
|---|---|---|---|
| Ethernet og MAC-adresse | [5-lags TCP/IP-modell – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/5-lags-tcpip-modell/9e31c212f6) og [svitsj – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/svitsj/a33b4b015c) | Hvordan er klienten koblet til det lokale nettverket? | nettverkskort, kabel eller trådløs forbindelse, svitsjport og MAC-adresse |
| ARP | [5-lags TCP/IP-modell – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/5-lags-tcpip-modell/9e31c212f6) | Hvilken MAC-adresse hører til en lokal IP-adresse? | ARP-tabell med [Windows- eller Linux-kommando](nettverkskommandoer.md) |
| IP-adresse og subnett | [IP-adresser – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/ip-adresser/3082395965) | Hvilken adresse har klienten, og hvilke adresser regnes som lokale? | [IP-adresse, subnettmaske eller prefiks](ip-og-subnett.md) |
| Standard gateway | [Ruter – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/ruter/eb2ce6553f) | Hvor sendes trafikk som skal til et annet nettverk? | gateway-adresse og kontroll av forbindelse til gateway |
| DHCP | [DHCP – Vg2](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dhcp/8755440e02) | Hvordan fikk klienten nettverkskonfigurasjonen? | DHCP-server og tildelte verdier med [aktuell kommando](nettverkskommandoer.md) |
| DNS | [DNS-oppslag – Vg2](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dns-oppslag/8b81c28535) | Hvordan blir et vertsnavn oversatt til en IP-adresse? | kontrollert navneoppslag med [aktuell kommando](nettverkskommandoer.md) |
| Tjeneste | [Nettverkstjenester og protokoller – Vg2](https://ndla.no/e/driftsstotte-im-itk-vg2/nettverkstjenester-og-protokoller/d4b104e3ab) | Svarer tjenesten som brukeren faktisk trenger? | [avtalt tjenestetest](tjenestetest.md) |

## Før du går videre

Du er klar for veiledet feilsøking når du kan:

- forklare funksjonen til hvert ledd med egne ord
- finne relevante verdier uten å lagre hemmeligheter eller unødvendige identifikatorer
- skille en observasjon fra en antakelse
- velge neste kontroll ut fra resultatet fra forrige kontroll
