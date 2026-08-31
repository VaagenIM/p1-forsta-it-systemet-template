# IP-adresse, subnett og standard gateway

Bruk denne siden når du skal avgjøre om et mål er på samme nett som klienten, eller om trafikken må sendes til standard gateway.

## IP-adresse og prefiks

En IPv4-adresse identifiserer et nettverksgrensesnitt. Prefikset viser hvor stor del av adressen som beskriver nettet.

Eksempel:

```text
IP-adresse: 192.168.10.25
Prefiks:     /24
```

Med `/24` er de tre første tallgruppene nettverksdelen. Nettet er da `192.168.10.0/24`.

Kilde: [IP-adresser - NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/ip-adresser/3082395965).

> **Kort sagt:** IP-adressen peker ut grensesnittet, mens prefikset viser hvilket nett det tilhører.

## Samme nett eller et annet nett

Sammenlign klientens adresse med måladressen.

| Klient | Mål | Vurdering |
|---|---|---|
| `192.168.10.25/24` | `192.168.10.80` | Samme nett: `192.168.10.0/24` |
| `192.168.10.25/24` | `192.168.20.10` | Annet nett |

I det første eksempelet kan klienten lete etter målets MAC-adresse med ARP. I det andre må klienten sende trafikken til standard gateway.

> **Kort sagt:** Samme nett betyr lokal levering. Et annet nett betyr levering via en ruter.

## Standard gateway

Standard gateway er ruteradressen klienten bruker når målet ikke ligger på klientens eget nett.

Eksempel:

```text
klient 192.168.10.25/24 -> standard gateway 192.168.10.1 -> mål 192.168.20.10
```

Gatewayen må normalt ha en adresse i samme lokale nett som klienten. Kontroller den observerte adressen med [`ipconfig /all` eller `ip route`](nettverkskommandoer.md).

Kilde: [Ruter - NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/ruter/eb2ce6553f).

> **Kort sagt:** Standard gateway er klientens vei til andre nettverk.

## Slik bruker du dette i laben

1. Finn klientens IP-adresse og subnettmaske eller prefiks.
2. Finn standard gateway.
3. Skriv opp det avtalte målets IP-adresse.
4. Avgjør om målet er lokalt eller ligger på et annet nett.
5. Kontroller vurderingen mot topologien og opplysningene fra den muntlige gjennomgangen.

Ikke gjett nett eller adresser som ikke er oppgitt eller observert.
