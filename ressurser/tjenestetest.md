# Test en tjeneste

Bruk denne siden når du skal kontrollere om den avtalte tjenesten faktisk svarer.

## Tjeneste, protokoll og port

En tjeneste er en funksjon en klient bruker. Protokollen beskriver hvordan klienten og tjenesten kommuniserer, og et portnummer kan peke trafikken til riktig tjeneste på verten.

Eksempler:

| Behov | Tjeneste eller protokoll | Vanlig test |
|---|---|---|
| slå opp et vertsnavn | DNS | `nslookup` eller `getent ahosts` |
| åpne en nettside | HTTP eller HTTPS | åpne avtalt URL i nettleseren |
| kontrollere ICMP-svar | ICMP | `ping` |

`ping` er en nettverkstest, ikke en full test av en nettside, DNS-tjeneste eller et annet program.

Kilde: [Nettverkstjenester og protokoller - NDLA Vg2](https://ndla.no/e/driftsstotte-im-itk-vg2/nettverkstjenester-og-protokoller/d4b104e3ab).

> **Kort sagt:** Test funksjonen brukeren trenger, ikke bare om en adresse svarer.

## Gjennomfør en avtalt test

1. Skriv hva brukeren skal kunne gjøre.
2. Finn avtalt vertsnavn eller IP-adresse, protokoll og eventuelt portnummer.
3. Skriv hvilket resultat du forventer.
4. Gjennomfør bare den avtalte testen.
5. Sammenlign faktisk resultat med forventet resultat.
6. Noter hva testen viser, og hva den ikke kan bevise alene.

Eksempel:

```text
Behov: Åpne den avtalte nettsiden.
Mål: https://avtalt-navn.example/
Forventet: Siden åpnes og viser avtalt innhold.
Faktisk: Nettleseren viste siden uten feilmelding.
Viser: HTTPS-tjenesten svarte på denne forespørselen.
Viser ikke alene: At alle tjenester på verten fungerer.
```

## Fra Linux-konsollen

Hvis læreren ber deg teste en avtalt HTTP- eller HTTPS-adresse fra en VM eller container, kan du hente bare svarhodet:

```bash
curl -I https://avtalt-navn.example/
```

Kommandoen sender en nettverksforespørsel. Bruk den bare mot avtalt mål. Hvis `curl` ikke finnes, skal du ikke installere programvare. Bruk en annen avtalt test eller be om veiledning.

Kilde: [`curl` manual](https://curl.se/docs/manpage.html).

## Dokumenter problemet og løsningen

Hvis testen ikke gir forventet resultat, fortsetter du med [nettverkskjeden](nettverkskjeden.md) og [feilsøkingsmetoden](feilsoking.md). Før sluttresultatet i `arbeid/feilsoking.md`:

- hvilke problemer eller feil oppsto
- hva du undersøkte
- hva årsaken var
- hvordan problemet ble løst
- hvordan du kontrollerte løsningen
