# Språk- og dokumentasjonskonvensjoner

## Norsk fagbegrep først

Skriv norsk fagbegrep først. Oppgi engelsk originalbegrep og eventuell forkortelse i parentes første gang begrepet brukes.

| Norsk fagbegrep | Engelsk originalbegrep |
|---|---|
| komponentoversikt | system component inventory |
| svitsj | switch |
| ruter | router |
| vertsmaskin | host |
| virtuell maskin | virtual machine, VM |
| versjonskontroll | version control |
| repo | repository |
| arkitekturbeslutning | architecture decision record, ADR |
| fysisk topologi | physical topology |
| logisk topologi | logical topology |

I dette repoet brukes **arkitektur** om systemhelheten, **infrastruktur** om det tekniske grunnlaget og **topologi** om plassering og forbindelser i diagrammene.

Bruk norske begreper eller en innarbeidet forkortelse konsekvent (har du brukt det en gang, bruker du det på samme måte neste gang). Behold kommandoer, filnavn og produktnavn uendret, for eksempel `git commit`, `README.md`, Proxmox VE og UniFi Network.

## Diagrammer

- Bruk samme navn eller ID i diagram, komponentoversikt og systemoversikt.
- Skill mellom **navn eller ID**, **type**, **rolle** og **teknisk verdi**.
- Merk viktige forbindelser med port, protokoll eller en presis relasjon.
- Erstatt alle `<...>`, spørsmålstegn og generiske startnavn før levering.
- Følg [standarden for etiketter i topologidiagrammer](diagrametiketter.md).

## Filnavn

- Behold `README.md` og `.gitignore` fordi Git-plattformen kjenner igjen disse navnene.
- Bruk korte norske ASCII-navn for øvrige filer.
- Ikke bruk mellomrom, `æ`, `ø` eller `å` i filnavn.
- Bruk bindestrek mellom ord, for eksempel `fysisk-topologi.drawio`.

## Git

- Kontroller hva som er endret før du registrerer endringen.
- Samle én meningsfull endring per `git commit`.
- Skriv kort på norsk om hva som ble endret.

Eksempler:

```text
docs: legg til fysisk server i komponentoversikten
docs: oppdater fysisk nettverksdiagram
docs: dokumenter DHCP og standard gateway
fix: rett feil IP-adresse i komponentoversikten
```

## Sikkerhet

Ikke legg passord, API-nøkler, private nøkler, personopplysninger eller andre hemmeligheter i repoet.

### Systemnavn og nettverksverdier

- Bruk systemnavnene og identifikatorene som blir oppgitt i den muntlige gjennomgangen.
- Lagre bare MAC-adresser, IP-adresser, vertsnavn og VLAN når du uttrykkelig har fått beskjed om at de kan dokumenteres.
- Bruk funksjonelle navn som `PC-01`, `SW-01`, `PVE-01` og `DNS-01` når virkelige navn ikke skal deles.
- Masker verdier ved behov, for eksempel `10.20.x.x` eller `AA:BB:CC:xx:xx:xx`.
- Ikke ta med brukernavn, elevnavn, påloggingstegn eller skjermbilder som viser uvedkommende systemer.
