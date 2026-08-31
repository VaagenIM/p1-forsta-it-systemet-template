# Linux-konsoll i Proxmox

Bruk denne siden når du skal observere Linux fra Proxmox VE-webgrensesnittet.

## Velg riktig konsoll

| Hvor du åpner konsollen | Hva du undersøker |
|---|---|
| Proxmox-node -> `Shell` | Den fysiske verten og Proxmox VE-operativsystemet |
| Virtuell maskin (VM) -> `Console` | Operativsystemet inne i den virtuelle maskinen |
| Container (CT) -> `Console` | Operativsystemmiljøet inne i containeren |

En kommando beskriver systemet den kjøres på. Et resultat fra VM-konsollen kan derfor ikke brukes som belegg for vertens nettverkskonfigurasjon.

> **Kort sagt:** Node Shell viser verten. VM- eller CT-konsollen viser gjesten.

## Kontroller hvor du er

Kjør disse før du samler nettverksinformasjon:

```bash
whoami
hostnamectl
cat /etc/os-release
```

Noter brukertype, vertsnavn og operativsystem. Ikke ta med brukernavn dersom det kan identifisere en person.

Kilder: [Debian Administrator's Handbook](https://debian-handbook.info/browse/stable/) og [Proxmox VE Administration Guide](https://pve.proxmox.com/pve-docs/pve-admin-guide.html).

## Tillatte observasjoner

| Kommando | Viser |
|---|---|
| `ip -brief address` | grensesnitt, status og IP-adresse/prefiks |
| `ip route` | lokale ruter og standardrute |
| `ip neigh` | observerte IP- og MAC-koblinger |
| `df -h` | monterte filsystemer og brukt lagringsplass |
| `free -h` | brukt og tilgjengelig arbeidsminne |

Se [nettverkskommandoer](nettverkskommandoer.md#linux-i-proxmox-konsollen) for hvordan nettverksresultatene tolkes.

## Ikke endre systemet

I denne perioden skal du ikke:

- installere eller oppdatere pakker uten at det er avtalt
- endre nettverk, brannmur, lagring, brukere eller tjenester
- starte, stoppe, opprette eller slette virtuelle ressurser
- kjøre nedlastede skript
- bruke kommandoer som `rm -r`, `dd`, `qm destroy` eller `pct destroy`

Stopp før du bruker `sudo` eller en kommando som kan skrive til systemet. Be læreren om godkjenning dersom oppgaven faktisk krever en endring.

> **Kort sagt:** Les og dokumenter. Ikke endre.

## Dokumenter et relevant utdrag

Skriv:

```text
Hvor kjørte jeg kommandoen:
Hva undersøkte jeg:
Kommando:
Relevant resultat:
Hva viser resultatet:
```

Ikke lim inn hele konsolløkten, hemmeligheter eller unødvendige identifikatorer.
