# Nettverkskommandoer

Bruk kommandoene til å observere nettverket uten å endre konfigurasjonen. Velg delen som passer til systemet du faktisk undersøker.

## Før du kjører en kommando

1. Kontroller om du arbeider på Windows-klienten, Proxmox-verten eller en virtuell maskin/container.
2. Bruk bare mål og adresser fra den muntlige gjennomgangen eller mål du allerede har bekreftet.
3. Noter spørsmålet kommandoen skal hjelpe deg å svare på.
4. Ta bare med relevante utdrag i dokumentasjonen.

## Windows-klient

### Finn nettverkskonfigurasjonen

```powershell
ipconfig /all
```

Se etter riktig nettverkskort og feltene fysisk adresse, IPv4-adresse, subnettmaske, standard gateway, DHCP-server og DNS-server. Ikke kopier hele resultatet.

Kilder: [enkelt oppsett av labnettverk - NDLA Vg2](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/enkelt-oppsett-av-labnettverk/00a06e8d31) og [`ipconfig` - Microsoft](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ipconfig).

### Se lokale IP- og MAC-koblinger

```powershell
arp -a
```

Finn bare den avtalte lokale IP-adressen. Tabellen viser observerte koblinger mellom IP- og MAC-adresser, men forteller ikke alene hvilken fysisk port enheten bruker.

Kilder: [5-lags TCP/IP-modell - NDLA Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/5-lags-tcpip-modell/9e31c212f6) og [`arp` - Microsoft](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/arp).

### Kontroller svar fra et avtalt mål

```powershell
ping 192.0.2.10
```

Bytt eksempeladressen med det avtalte målet. Svar viser at ICMP-testen lyktes. Manglende svar beviser ikke alene at maskinen eller tjenesten er nede.

Kilde: [`ping` - Microsoft](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ping).

### Kontroller navneoppslag

```powershell
nslookup avtalt-navn.example
```

Se etter hvilken DNS-server som svarte, og hvilken IP-adresse navnet ble slått opp til. Bruk bare vertsnavn læreren har godkjent.

Kilder: [DNS-oppslag - NDLA Vg2](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dns-oppslag/8b81c28535) og [`nslookup` - Microsoft](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/nslookup).

## Linux i Proxmox-konsollen

Les først [Linux-konsoll i Proxmox](linux-konsoll.md), slik at du vet om kommandoen kjøres på verten eller i en gjest.

| Spørsmål | Kommando | Se etter |
|---|---|---|
| Hvilke adresser har grensesnittene? | `ip -brief address` | grensesnittnavn, status og IP-adresse/prefiks |
| Hvilken vei brukes ut av nettet? | `ip route` | lokalt nett, `default via` og grensesnitt |
| Hvilke lokale naboer er observert? | `ip neigh` | IP-adresse, MAC-adresse og tilstand |
| Svarer et avtalt mål? | `ping -c 4 192.0.2.10` | mottatte svar og pakketap |
| Hvilken adresse får et navn? | `getent ahosts avtalt-navn.example` | adressene navnet blir slått opp til |
| Hvilke DNS-innstillinger brukes? | `resolvectl status` | DNS-server per grensesnitt |

Hvis `resolvectl` ikke finnes, kan du lese `cat /etc/resolv.conf`. Det viser en resolverkonfigurasjon, men filen kan være generert av en annen tjeneste.

Kilder: [`ip-address`](https://manpages.debian.org/stable/iproute2/ip-address.8.en.html), [`ip-route`](https://manpages.debian.org/stable/iproute2/ip-route.8.en.html), [`ip-neighbour`](https://manpages.debian.org/stable/iproute2/ip-neighbour.8.en.html) og [`getent`](https://manpages.debian.org/stable/manpages/getent.1.en.html) i Debian.

## Tolk resultatet før neste test

| Observasjon | Dette kan den støtte | Dette beviser den ikke alene |
|---|---|---|
| Klienten har forventet IP og prefiks | nettverkskortet har en IP-konfigurasjon | at gateway, DNS eller tjenesten virker |
| Gateway svarer på `ping` | ICMP når gatewayadressen og et svar kommer tilbake | at DNS eller måltjenesten virker |
| Navnet blir slått opp | DNS-oppslaget gir en adresse | at tjenesten på adressen virker |
| Tjenestetesten lykkes | den avtalte tjenesten svarer på valgt måte | at alle andre tjenester på verten virker |

Fortsett med [IP og subnett](ip-og-subnett.md), [nettverkskjeden](nettverkskjeden.md) eller [tjenestetest](tjenestetest.md) ut fra spørsmålet du undersøker.
