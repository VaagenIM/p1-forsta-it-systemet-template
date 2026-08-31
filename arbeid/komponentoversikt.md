# Komponentoversikt
*system component inventory*

Komponentoversikten skal beskrive **hele IT-laben**, men du begynner med komponentene ved egen stasjon. Følg deretter forbindelsene videre til felles nettverksutstyr, servere, virtuelle ressurser og tjenester.

Oppdater oversikten når komponenter legges til, fjernes eller endres.

Skriv i kolonnen `Merknad` hvordan du fant informasjonen. Bruk [begrepene i komponentoversikten](../ressurser/begreper-i-komponentoversikten.md) når du er usikker på et felt, og følg [reglene for systemnavn og nettverksverdier](../ressurser/konvensjoner.md#systemnavn-og-nettverksverdier). Bruk samme navn eller ID i [topologidiagrammene](../ressurser/diagrametiketter.md).

Se [eksempel på en komponentrad](../ressurser/eksempler.md#komponentrad) før du fyller ut tabellene.

## Fysiske maskiner

| Navn eller ID | Type | Rolle | Modell | Operativsystem | Plassering | Merknad |
| ------------- | ---- | ----- | ------ | -------------- | ---------- | ------- |
|               |      |       |        |                |            |         |

## Nettverksutstyr

| Navn eller ID | Type | Rolle | Modell | Plassering | Merknad |
| ------------- | ---- | ----- | ------ | ---------- | ------- |
|               |      |       |        |            |         |

## Nettverksgrensesnitt

| Komponent | Grensesnitt | MAC-adresse | IP-adresse | Subnettmaske eller prefiks | Nett eller VLAN | Merknad |
|---|---|---|---|---|---|---|
| | | | | | | |

## Nettverksinnstillinger og tjenester

| Komponent | Standard gateway | DHCP-server | DNS-server | Merknad |
|---|---|---|---|---|
| | | | | |

## Virtuelle komponenter

| Navn eller ID | Type | Rolle | Vertsmaskin (host) | Operativsystem | Nettverk | Merknad |
|---|---|---|---|---|---|---|
| | | | | | | |

## Tjenester

| Tjeneste | Kjører på | Rolle eller hensikt | Protokoll eller port | Avhengigheter | Merknad |
|---|---|---|---|---|---|
| | | | | | |

## Relasjoner og avhengigheter

Bruk denne delen når en viktig relasjon/avhengighet ikke kommer tydelig fram i tabellene over.

Eksempler:

- `VM-01` **kjører på** `PVE-01`
- `PC-01` **er koblet til** `SW-01`
- `PC-01` **bruker** `DNS-01`
- `WEB-01` **er avhengig av** `DNS`
