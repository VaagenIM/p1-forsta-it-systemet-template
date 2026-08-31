# Finn virtuell og fysisk infrastruktur i Proxmox VE

Bruk denne siden for å følge en avtalt virtuell ressurs fra Proxmox VE til verten og nettverket. Arbeidet er lesende: ikke endre konfigurasjonen.

## Begrepene i webgrensesnittet

| Begrep | Betydning |
|---|---|
| Datasenter (`Datacenter`) | samlingen av Proxmox-noder og felles innstillinger |
| Node | fysisk server som kjører Proxmox VE |
| Virtuell maskin (VM) | eget gjesteoperativsystem med virtuelle ressurser |
| Container (CT) | isolert miljø som deler Linux-kjernen med verten |
| Lagring (`Storage`) | stedet virtuelle disker, ISO-filer eller sikkerhetskopier lagres |
| Linux-bro (`vmbrX`) | virtuell svitsj som kan koble gjester til vertens fysiske nettverk |

Kilder: [Virtuelle maskiner - NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelle-maskiner/b8a976125b) og [Proxmox VE Administration Guide](https://pve.proxmox.com/pve-docs/pve-admin-guide.html).

> **Kort sagt:** Noden er den fysiske verten. VM og CT er virtuelle gjester som bruker vertens ressurser.

## Finn ressursen

1. Velg den avtalte noden i venstremenyen.
2. Åpne `Summary` og finn nodens navn og status.
3. Velg den avtalte VM-en eller containeren.
4. Finn ID, navn, status, prosessor, arbeidsminne og disk i `Summary` eller `Hardware`.
5. Finn nettverksenheten i `Hardware` og noter modell, MAC-adresse og valgt bro når opplysningene kan dokumenteres.
6. Åpne nodens nettverksvisning og finn den samme Linux-broen, for eksempel `vmbr0`. Ikke trykk `Apply Configuration`.
7. Kontroller funnene mot komponentoversikten og topologidiagrammene.

Menynavn kan variere noe med Proxmox-versjon og tilgangsnivå. Bruk funksjonen som beskrives, og be om veiledning hvis den ikke er synlig.

## Følg avhengigheten

En vanlig brokoblet VM kan følges slik:

```text
tjeneste -> VM eller CT -> virtuelt nettverkskort -> Linux-bro -> fysisk nettverkskort -> fysisk nettverk
```

Proxmox beskriver Linux-broen som en virtuell svitsj. En gjests virtuelle nettverkskort kan kobles til broen, og broen kan være koblet til vertens fysiske nettverkskort.

Kilde: [Network Configuration - Proxmox VE Administration Guide](https://pve.proxmox.com/pve-docs/pve-admin-guide.html#sysadmin_network_configuration).

> **Kort sagt:** Følg tjenesten fra gjesten gjennom det virtuelle nettverkskortet og broen til vertens fysiske nett.

## Bruk konsollen riktig

- Bruk node -> `Shell` når du skal observere verten.
- Bruk VM eller CT -> `Console` når du skal observere gjesten.
- Følg [Linux-konsoll i Proxmox](linux-konsoll.md) før du kjører kommandoer.

## Dette dokumenterer du

Før bare inn opplysninger som er relevante og tillatt:

- node og gjestetype
- VM-/CT-ID og funksjonelt navn
- operativsystem
- tildelt prosessor, arbeidsminne og disk
- virtuelt nettverkskort, bro og aktuelt nett/VLAN
- tjenesten som kjører på gjesten
- relasjonen til fysisk vert og nettverk

Ikke dokumenter passord, nøkler eller identifiserende opplysninger som oppgaven ikke trenger.
