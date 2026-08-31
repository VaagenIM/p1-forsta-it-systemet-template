# Eksempler

Eksemplene viser form og detaljnivå. Verdiene er oppdiktet og skal ikke kopieres som fakta om IT-laben.

## Komponentrad

| Navn eller ID | Type   | Rolle          | Modell                   | Operativsystem | Plassering | Merknad                        |
| ------------- | ------ | -------------- | ------------------------ | -------------- | ---------- | ------------------------------ |
| `PC-01`       | klient | arbeidsstasjon | Eksempelmodell 1000 | Windows 11 | stasjon 12 | lest fra etiketten på maskinen |

En god rad skiller mellom hva komponenten **er**, hvilken **rolle** den har, og hvordan opplysningen ble funnet.

## Problem og løsning

- **Hva oppsto?** Et avtalt vertsnavn kunne ikke åpnes, men tjenestens IP-adresse svarte på `ping`.
- **Hva undersøkte eller prøvde du?** Kontrollerte IP-adresse og DNS-server med `ipconfig /all`, og testet navnet med `nslookup`.
- **Hva var årsaken?** Klienten brukte feil DNS-adresse i det kontrollerte feilscenarioet.
- **Hvordan løste du problemet?** Den avtalte DNS-adressen ble gjenopprettet med tillatelse.
- **Hvordan kontrollerte du løsningen?** `nslookup` ga riktig IP-adresse, og tjenesten kunne åpnes med vertsnavnet.
- **Hva lærte du?** En fungerende IP-forbindelse betyr ikke at navneoppslaget virker.

## Diagrammer

**Fysisk topologi** viser faktiske enheter, porter, kabler og plasseringer.

```text
PC-01 -> svitsjport 8 -> SW-01 -> ruter
                         `--> PVE-01
```

**Logisk topologi** viser nett, VLAN, standard gateway, tjenester og logiske avhengigheter.

```text
klientnett -> standard gateway -> servernett -> tjeneste
     └──────────── bruker DNS ──────────────┘
```

Bruk samme navn i komponentoversikten, diagrammene og systemoversikten. Merk usikre opplysninger med `?` til de er bekreftet.

## Kildelisterad

| Kilde og lenke | Hva fant du? | Hvor brukte du det? |
|---|---|---|
| NDLA: IP-adresser | forskjellen mellom nettverksdel og vertsdel | forklaringen av klientnettet i systemoversikten |
