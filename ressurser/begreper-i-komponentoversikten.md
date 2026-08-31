# Begreper i komponentoversikten

Bruk siden som et oppslagsverk når du fyller ut [komponentoversikten](../arbeid/komponentoversikt.md). Gå direkte til delen som forklarer feltet eller begrepet du arbeider med.

## Finn begrepet

- **Fysiske komponenter:** [navn eller ID](#navn-eller-id), [type](#type), [rolle](#rolle), [modell](#modell), [operativsystem](#operativsystem), [plassering](#plassering) og [merknad](#merknad)
- **Nettverk:** [grensesnitt](#grensesnitt), [MAC-adresse](#mac-adresse), [IP-adresse](#ip-adresse), [subnettmaske eller prefiks](#subnettmaske-eller-prefiks), [nett eller VLAN](#nett-eller-vlan), [standard gateway](#standard-gateway), [DHCP-server](#dhcp-server), [DNS-server](#dns-server), [svitsj](#svitsj) og [ruter](#ruter)
- **Virtualisering:** [virtuell maskin](#virtuell-maskin), [vertsmaskin](#vertsmaskin) og [nettverk for virtuelle komponenter](#nettverk-for-virtuelle-komponenter)
- **Tjenester og sammenhenger:** [tjeneste](#tjeneste), [kjører på](#kjører-på), [rolle eller hensikt](#rolle-eller-hensikt), [protokoll](#protokoll), [port](#port), [relasjon](#relasjon) og [avhengighet](#avhengighet)

En **komponentoversikt** (*system component inventory*) beskriver hvilke deler et IT-system består av, hvor de befinner seg, hvilken funksjon de har, og hvordan de henger sammen.

En komponent kan for eksempel være:

* en fysisk datamaskin
* en server
* en svitsj
* en ruter
* en virtuell maskin
* en container
* en tjeneste

Oversikten skal gjøre det mulig for andre å forstå systemet og finne igjen komponentene som inngår i det.

NDLA anbefaler blant annet å dokumentere servernavn, funksjon, IP-adresser, operativsystem, nettverksutstyr, nettverkstjenester og fysisk infrastruktur. NIST bruker begrepet **System Component Inventory** om en dokumentert oversikt over identifiserbare komponenter som utgjør et system.

**Les mer:**

* [NDLA – Hva bør du dokumentere i IT-systemer?](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0)
* [NIST – Information System Component Inventory](https://csrc.nist.gov/glossary/term/information_system_component_inventory)
* [NIST SP 800-171 – System Component Inventory](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/800-171r3/NIST.SP.800-171r3.html#req_03_04_10)

> **Kort sagt:** Komponentoversikten er kartoteket over delene som utgjør IT-systemet.

---

## Fysiske komponenter

### Navn eller ID

**Navn eller ID** er betegnelsen vi bruker for å identifisere én bestemt komponent.

Eksempler:

* `PC-01`
* `SW-01`
* `PVE-01`
* `VM-01`
* `DNS-01`

Navnet skal gjøre det mulig å skille komponenten fra andre komponenter.

Et godt navn eller en god ID bør være:

* entydig
* kort
* konsekvent
* brukt på samme måte gjennom hele dokumentasjonen

Hvis komponenten allerede har et godkjent systemnavn, bør dette brukes når det passer med navnekonvensjonene for systemet.

NDLA framhever at utstyr, kabler og koblingspunkter bør ha unike ID-er, og at blant annet servernavn skal inngå i systemdokumentasjonen.

**Les mer:**

* [NDLA – Hva bør du dokumentere i IT-systemer?](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0)

> **Kort sagt:** Navn eller ID svarer på spørsmålet **«Hvilken komponent er dette?»**

---

### Type

**Type** beskriver **hva slags komponent dette er**.

Eksempler:

* klient
* server
* svitsj
* ruter
* brannmur
* aksesspunkt
* virtuell maskin
* container

I denne komponentoversikten bruker vi `Type` som en kategori for å skille forskjellige slags komponenter fra hverandre.

Eksempel:

| Navn     | Type            |
| -------- | --------------- |
| `PC-01`  | klient          |
| `SW-01`  | svitsj          |
| `PVE-01` | server          |
| `VM-01`  | virtuell maskin |

NDLA skiller på samme måte mellom blant annet klientmaskiner, servere, rutere, svitsjer og virtuelle maskiner når IT-systemer beskrives.

**Les mer:**

* [NDLA – Datalab med Windows Server og generisk nettverk](https://ndla.no/r/driftsstotte-im-itk-vg2/datalab-med-windows-server-og-generisk-nettverk/6fbbe0f727)
* [NDLA – Virtuelle maskiner](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelle-maskiner/b8a976125b)

> **Kort sagt:** Type svarer på spørsmålet **«Hva er komponenten?»**

---

### Rolle

**Rolle** beskriver **hva komponenten gjør i systemet**.

Eksempler:

* arbeidsstasjon
* virtualiseringsvert
* webserver
* filserver
* databaseserver
* DNS-server
* DHCP-server
* gateway
* brannmur

En komponent kan ha flere roller.

Eksempel:

| Navn     | Type   | Rolle               |
| -------- | ------ | ------------------- |
| `PC-01`  | klient | arbeidsstasjon      |
| `PVE-01` | server | virtualiseringsvert |
| `SRV-01` | server | webserver           |
| `SW-01`  | svitsj | aksess-svitsj       |

NDLA bruker blant annet **funksjon** når servere skal dokumenteres, med eksempler som filserver, e-postserver og webserver. I vår komponentoversikt kaller vi dette feltet `Rolle`.

**Les mer:**

* [NDLA – Hva bør du dokumentere i IT-systemer?](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0)

> **Kort sagt:** Rolle svarer på spørsmålet **«Hva gjør komponenten?»**

---

### Type og rolle er ikke det samme

Det er viktig å skille mellom type og rolle.

```text
Type  = hva komponenten er
Rolle = hva komponenten gjør
```

For eksempel:

```text
PVE-01
Type:  server
Rolle: virtualiseringsvert
```

En annen server kan ha:

```text
DB-01
Type:  server
Rolle: databaseserver
```

Begge er altså av typen `server`, men de har forskjellige roller.

> **Kort sagt:** To komponenter kan være samme type, men gjøre helt forskjellige oppgaver.

---

### Modell

**Modell** beskriver hvilken maskinvaremodell eller produktmodell komponenten er.

Eksempler:

* `HP EliteDesk 800 G5 Mini`
* `Dell PowerEdge R640`
* `UniFi USW-24`
* `MikroTik CRS305-1G-4S+IN`

Modell er noe annet enn navn eller ID.

For eksempel:

| Navn eller ID | Modell                   |
| ------------- | ------------------------ |
| `PC-01`       | HP EliteDesk 800 G5 Mini |
| `PC-02`       | HP EliteDesk 800 G5 Mini |

To komponenter kan derfor ha samme modell, men skal fremdeles kunne identifiseres som to forskjellige komponenter.

NDLA anbefaler at maskinvareinformasjon inngår i systemdokumentasjonen.

**Les mer:**

* [NDLA – Hva bør du dokumentere i IT-systemer?](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0)

> **Kort sagt:** Modell forteller **hvilket produkt komponenten er**.

---

### Operativsystem

Et **operativsystem** (*operating system, OS*) er grunnleggende programvare som styrer og fordeler ressursene i en datamaskin. Det ligger mellom maskinvaren og programmene som kjører på maskinen.

Eksempler:

* Windows 11
* Debian 13
* Ubuntu Server
* Proxmox VE
* Windows Server

Ta gjerne med versjon når den er kjent.

```text
Debian 13
```

NDLA beskriver blant annet at operativsystemet håndterer ressurser, sikkerhet, brukere, enhetsdrivere, nettverk og brukergrensesnitt.

**Les mer:**

* [NDLA – Operativsystem](https://ndla.no/nb/r/teknologiforstaelse-im-ikm-vg1/operativsystem/c04d611412)

> **Kort sagt:** Operativsystemet er grunnlaget som gjør at programmene kan bruke maskinvaren.

---

### Plassering

**Plassering** beskriver hvor den fysiske komponenten befinner seg.

Eksempler:

* `stasjon 12`
* `stasjon 4`
* `rack A, U12`
* `teknisk rom`
* `lærerpult`

Plassering bør være så presis at en annen person kan finne komponenten.

NDLA anbefaler blant annet at plasseringen av sentrale koblingspunkter, kabler og annet fysisk utstyr dokumenteres.

**Les mer:**

* [NDLA – Hva bør du dokumentere i IT-systemer?](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0)

> **Kort sagt:** Plassering svarer på spørsmålet **«Hvor finner jeg komponenten?»**

---

### Merknad

**Merknad** er et fritekstfelt for relevant informasjon som ikke passer naturlig i de andre feltene.

I denne oppgaven brukes feltet også til å dokumentere **hvordan informasjonen ble funnet eller kontrollert**.

Eksempler:

* `observert fysisk`
* `lest fra etiketten på maskinen`
* `systemnavn kontrollert i Windows`
* `IP-adresse funnet med ipconfig`
* `modellnummer ikke synlig`
* `systemnavn ikke verifisert`
* `midlertidig installasjon`
* `ikke i produksjon`
* `må undersøkes nærmere`

Dersom informasjonen er usikker, skal du skrive dette i stedet for å gjette.

For eksempel:

```text
Rolle ikke verifisert
```

Dette feltet er en **lokal dokumentasjonskonvensjon** i oppgaven, men bygger på prinsippet om at teknisk dokumentasjon skal være presis og gjøre det mulig å forstå og kontrollere systemet.

**Les mer:**

* [NDLA – Hva bør du dokumentere i IT-systemer?](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0)

> **Kort sagt:** Bruk merknad til det leseren **bør vite i tillegg**, særlig usikkerhet og hvordan informasjonen ble funnet.

---

## Nettverksinformasjon

### Komponent

Feltet **Komponent** viser hvilken komponent nettverksinformasjonen tilhører.

Eksempel:

```text
PC-01
```

Navnet skal være det samme som brukes i resten av komponentoversikten. Slik kan informasjon i forskjellige tabeller kobles sammen.

**Les mer:**

* [NDLA – Hva bør du dokumentere i IT-systemer?](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0)

> **Kort sagt:** Feltet kobler nettverksinformasjonen til riktig komponent.

---

### Grensesnitt

Et **nettverksgrensesnitt** (*network interface*) er forbindelsen en komponent bruker for å kommunisere med et nettverk.

Det kan for eksempel være:

* et fysisk Ethernet-kort
* et trådløst nettverkskort
* et virtuelt nettverkskort
* et VLAN-grensesnitt

Eksempler på grensesnittnavn:

```text
eth0
eno1
ens18
Wi-Fi
```

En maskin kan ha flere nettverksgrensesnitt og derfor også flere IP- og MAC-adresser.

**Les mer:**

* [NDLA – Statisk IP-adresse i Windows Server](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/datalab-med-windows-server-og-generisk-nettverk/6fbbe0f727/15092)

> **Kort sagt:** Nettverksgrensesnittet er komponentens **tilkoblingspunkt mot nettverket**.

---

### MAC-adresse

En **MAC-adresse** (*Media Access Control address*) identifiserer et nettverksgrensesnitt på datalinklaget.

Eksempel:

```text
00:1A:2B:3C:4D:5E
```

En datamaskin med Ethernet og Wi-Fi vil normalt ha forskjellige MAC-adresser for de to nettverksgrensesnittene.

Svitsjer bruker MAC-adresser for å finne ut hvilken fysisk svitsjport datapakker skal sendes videre gjennom.

**Les mer:**

* [NDLA – Svitsj](https://ndla.no/r/driftsstotte-im-itk-vg2/svitsj/a33b4b015c)
* [NDLA – Henting av MAC-adresser](https://ndla.no/r/teknologi-tp-pin-vg2/henting-av-mac-adresser/3ba19d897f)

> **Kort sagt:** MAC-adressen identifiserer **nettverksgrensesnittet i lokalnettet**.

---

### IP-adresse

En **IP-adresse** (*Internet Protocol address*) brukes til å adressere datapakker i lokale nettverk og over internett.

Eksempel på IPv4:

```text
192.168.10.25
```

Eksempel på IPv4 med prefiks:

```text
192.168.10.25/24
```

Det finnes to IP-standarder i vanlig bruk:

* IPv4
* IPv6

En IP-adresse kan være konfigurert manuelt eller tildelt automatisk, for eksempel ved hjelp av DHCP.

**Les mer:**

* [NDLA – IP-adresser](https://ndla.no/r/driftsstotte-im-itk-vg2/ip-adresser/3082395965)

> **Kort sagt:** IP-adressen brukes for å finne **riktig enhet i et IP-nettverk**.

---

### Subnettmaske eller prefiks

**Subnettmasken** eller **prefikset** viser hvilken del av IP-adressen som beskriver nettverket.

For IPv4 kan dette for eksempel skrives som:

```text
255.255.255.0
```

eller med CIDR-notasjon:

```text
/24
```

Dermed kan IP-adresse og prefiks skrives samlet:

```text
192.168.10.25/24
```

Prefikset brukes blant annet til å avgjøre hvilke IP-adresser som tilhører samme nettverk.

**Les mer:**

* [NDLA – IP-adresser](https://ndla.no/r/driftsstotte-im-itk-vg2/ip-adresser/3082395965)
* [NDLA – IPv4](https://ndla.no/nb/r/teknologiforstaelse-im-ikm-vg1/ipv4/018c76ed9c)

> **Kort sagt:** Prefikset forteller **hvilken del av IP-adressen som beskriver nettverket**.

---

### Nett eller VLAN

Feltet beskriver hvilket logisk nettverk komponenten tilhører.

Eksempler:

```text
VLAN 10
VLAN 20
Klientnett
Servernett
Administrasjonsnett
```

Et **VLAN** (*Virtual Local Area Network*) gjør det mulig å opprette flere adskilte logiske nettverk på det samme fysiske nettverksutstyret.

VLAN brukes blant annet for:

* segmentering
* tilgangskontroll
* bedre oversikt
* økt sikkerhet

Den sentrale åpne standarden for VLAN-merking i Ethernet er **IEEE 802.1Q**.

**Les mer:**

* [NDLA – Virtuelt lokalnettverk (VLAN)](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelt-lokalnettverk-vlan/9d865afa88)
* [IEEE – 802.1Q](https://standards.ieee.org/standard/802_1Q-2022.html)

> **Kort sagt:** VLAN deler ett fysisk nettverk inn i **flere logiske nettverk**.

---

### Standard gateway

En **standard gateway** (*default gateway*) er ruteren en komponent vanligvis sender datapakker til når mottakeren befinner seg utenfor det lokale nettverket.

Eksempel:

```text
IP-adresse:       192.168.10.25
Prefiks:          /24
Standard gateway: 192.168.10.1
```

Gateway-adressen er vanligvis en IP-adresse på ruteren i det aktuelle subnettet.

**Les mer:**

* [NDLA – DHCP](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dhcp/8755440e02)
* [NDLA – Ruter](https://ndla.no/r/driftsstotte-im-itk-vg2/ruter/eb2ce6553f)

> **Kort sagt:** Gatewayen er **veien ut av det lokale nettverket**.

---

### DHCP-server

**DHCP** (*Dynamic Host Configuration Protocol*) er en nettverkstjeneste som automatisk kan gi klienter nettverksinnstillinger.

Dette kan blant annet være:

* IP-adresse
* subnettmaske eller prefiks
* standard gateway
* DNS-server

Alternativet er å konfigurere informasjonen manuelt med statiske adresser.

**Les mer:**

* [NDLA – DHCP](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dhcp/8755440e02)

> **Kort sagt:** DHCP gjør at klienten kan få **nettverksinnstillingene automatisk**.

---

### DNS-server

**DNS** (*Domain Name System*) er systemet som gjør det mulig å bruke domenenavn i stedet for å måtte huske IP-adresser.

For eksempel kan DNS finne IP-adressen som hører til:

```text
www.ndla.no
```

Når en klient trenger å finne adressen til et navn, utfører den et **DNS-oppslag**.

DNS brukes både på internett og internt i virksomhetsnettverk.

**Les mer:**

* [NDLA – DNS-oppslag](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dns-oppslag/8b81c28535)
* [NDLA – Installasjon av DNS-server](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/installasjon-av-dns-server/4246401a38)

> **Kort sagt:** DNS gjør om **navn til adresser**.

---

## Nettverksutstyr

### Svitsj

En **svitsj** (*switch*) kobler sammen enheter i et lokalnettverk.

Svitsjen undersøker MAC-adressene i trafikken og bruker denne informasjonen til å sende trafikken videre gjennom riktig fysisk port.

De fleste vanlige svitsjer arbeider hovedsakelig på datalinklaget i TCP/IP-modellen.

**Les mer:**

* [NDLA – Svitsj](https://ndla.no/r/driftsstotte-im-itk-vg2/svitsj/a33b4b015c)

> **Kort sagt:** Svitsjen kobler sammen **enheter i lokalnettet**.

---

### Ruter

En **ruter** (*router*) kobler sammen forskjellige IP-nettverk og sender datapakker mellom dem.

Et vanlig eksempel er en ruter som kobler et lokalnettverk til internett.

Ruteren bruker blant annet:

* mottakerens IP-adresse
* informasjon om nettverk
* rutingtabeller

for å avgjøre hvor trafikken skal sendes videre.

**Les mer:**

* [NDLA – Ruter](https://ndla.no/r/driftsstotte-im-itk-vg2/ruter/eb2ce6553f)

> **Kort sagt:** Ruteren kobler sammen **forskjellige nettverk**.

---

## Virtuelle komponenter

### Virtuell maskin

En **virtuell maskin** (*virtual machine, VM*) er en programvarebasert datamaskin som får tildelt virtuelle ressurser fra en fysisk maskin.

Dette kan blant annet være:

* prosessorkraft
* arbeidsminne
* lagring
* nettverksgrensesnitt

Flere virtuelle maskiner kan kjøre på samme fysiske server.

**Les mer:**

* [NDLA – Virtuelle maskiner](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelle-maskiner/b8a976125b)
* [NDLA – Virtualisering av IT-ressurser](https://ndla.no/nb/e/driftsstotte-im-itk-vg2/virtualisering-av-it-ressurser/8f6a4829a0)

> **Kort sagt:** En VM er **en datamaskin realisert gjennom virtualisering**.

---

### Vertsmaskin

En **vertsmaskin** (*host*) er maskinen som stiller ressurser til rådighet for virtuelle maskiner.

Eksempel:

```text
VM-01 kjører på PVE-01
```

Her er:

* `VM-01` den virtuelle maskinen
* `PVE-01` vertsmaskinen

På en virtualiseringsplattform er det hypervisoren som fordeler ressursene mellom de virtuelle maskinene.

**Les mer:**

* [NDLA – Virtuelle maskiner](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelle-maskiner/b8a976125b)

> **Kort sagt:** Vertsmaskinen er **maskinen de virtuelle maskinene kjører på**.

---

### Nettverk for virtuelle komponenter

Virtuelle maskiner trenger også nettverksforbindelser.

Et virtuelt nettverksgrensesnitt kan for eksempel være koblet til:

```text
VLAN 20
Servernett
vmbr0
```

Den virtuelle maskinen kan dermed være koblet til samme logiske nettverksstruktur som fysiske maskiner.

**Les mer:**

* [NDLA – Virtuelle maskiner](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelle-maskiner/b8a976125b)
* [NDLA – Virtuelt lokalnettverk (VLAN)](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelt-lokalnettverk-vlan/9d865afa88)

> **Kort sagt:** Virtuelle maskiner trenger **virtuelle nettverksforbindelser** på samme måte som fysiske maskiner trenger fysiske.

---

## Tjenester

### Tjeneste

En **tjeneste** (*service*) er en funksjon et IT-system tilbyr til brukere, programmer eller andre systemer.

Eksempler:

* DNS
* DHCP
* web
* database
* fillagring
* SSH
* autentisering

En tjeneste må kjøre på en fysisk eller virtuell komponent.

NDLA understreker at servere først og fremst finnes fordi vi ønsker å levere tjenester til brukerne.

**Les mer:**

* [NDLA – Forskjellige typer skytjenester](https://ndla.no/r/driftsstotte-im-itk-vg2/forskjellige-typer-skytjenester/406e35111a)
* [NDLA – Mikrotjenester](https://ndla.no/en/r/driftsstotte-im-itk-vg2/mikrotjenester/129625ffae)

> **Kort sagt:** En tjeneste er **noe systemet gjør tilgjengelig for andre**.

---

### Kjører på

Feltet **Kjører på** viser hvilken komponent som faktisk leverer tjenesten.

Eksempel:

| Tjeneste   | Kjører på |
| ---------- | --------- |
| DNS        | `DNS-01`  |
| web        | `WEB-01`  |
| PostgreSQL | `DB-01`   |

Dette gjør det mulig å skille mellom:

```text
komponenten
```

og:

```text
tjenesten komponenten leverer
```

**Les mer:**

* [NDLA – Forskjellige typer skytjenester](https://ndla.no/r/driftsstotte-im-itk-vg2/forskjellige-typer-skytjenester/406e35111a)

> **Kort sagt:** Feltet forteller **hvor tjenesten faktisk kjører**.

---

### Rolle eller hensikt

**Rolle eller hensikt** beskriver hvorfor tjenesten finnes og hvilken oppgave den utfører.

Eksempler:

| Tjeneste   | Rolle eller hensikt                  |
| ---------- | ------------------------------------ |
| DNS        | oversette domenenavn til IP-adresser |
| DHCP       | tildele nettverksinnstillinger       |
| PostgreSQL | lagre data                           |
| webserver  | levere nettinnhold                   |

Dette er viktig fordi navnet på en tjeneste ikke alltid forklarer hvorfor den brukes i akkurat dette systemet.

**Les mer:**

* [NDLA – Hva bør du dokumentere i IT-systemer?](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0)

> **Kort sagt:** Hensikten forklarer **hvorfor tjenesten finnes i systemet**.

---

### Protokoll

En **protokoll** er et felles regelsett som systemer bruker når de kommuniserer.

Eksempler:

* Ethernet
* IP
* TCP
* UDP
* HTTP
* DNS
* DHCP
* SSH

Forskjellige protokoller har forskjellige oppgaver. TCP/IP-modellen brukes til å vise hvordan flere slike protokoller arbeider sammen.

**Les mer:**

* [NDLA – TCP/IP-modellen](https://ndla.no/nn/r/driftsstotte-im-itk-vg2/5-lags-tcpip-modell/9e31c212f6)
* [NDLA – TCP, UDP og porter](https://ndla.no/r/driftsstotte-im-itk-vg2/tcp-udp-og-porter/d7acb2196e)

> **Kort sagt:** En protokoll er **reglene for kommunikasjonen**.

---

### Port

Et **portnummer** brukes sammen med blant annet TCP og UDP for å angi hvilket program eller hvilken tjeneste nettverkstrafikken skal leveres til.

Eksempler:

| Tjeneste | Protokoll | Standardport |
| -------- | --------- | -----------: |
| SSH      | TCP       |           22 |
| DNS      | UDP/TCP   |           53 |
| HTTP     | TCP       |           80 |
| HTTPS    | TCP       |          443 |

Standardporter kan endres. Derfor skal du dokumentere den **faktiske konfigurasjonen** når du kan undersøke den.

**Les mer:**

* [NDLA – TCP, UDP og porter](https://ndla.no/r/driftsstotte-im-itk-vg2/tcp-udp-og-porter/d7acb2196e)
* [IANA – Service Name and Transport Protocol Port Number Registry](https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml)

> **Kort sagt:** IP-adressen finner **maskinen**, mens portnummeret hjelper med å finne **riktig tjeneste på maskinen**.

---

## Relasjoner og avhengigheter

### Relasjon

En **relasjon** beskriver hvordan to komponenter eller tjenester henger sammen.

Eksempler:

```text
VM-01 kjører på PVE-01
PC-01 er koblet til SW-01
PC-01 bruker DNS-01
SW-01 er koblet til RTR-01
```

Relasjoner gjør at dokumentasjonen ikke bare viser **hvilke komponenter som finnes**, men også hvordan systemet er bygget opp.

NDLA bruker nettverksmodeller og systemdokumentasjon nettopp for å synliggjøre hvordan utstyr og tjenester er koblet sammen.

**Les mer:**

* [NDLA – Hva bør du dokumentere i IT-systemer?](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0)
* [NDLA – Enkelt oppsett av labnettverk](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/enkelt-oppsett-av-labnettverk/00a06e8d31)

> **Kort sagt:** En relasjon beskriver **hvordan to deler av systemet henger sammen**.

---

### Avhengighet

En **avhengighet** betyr at en komponent eller tjeneste trenger en annen komponent eller tjeneste for å fungere som forventet.

Eksempel:

```text
WEB-01 er avhengig av DB-01
```

En webapplikasjon kan for eksempel være avhengig av:

```text
webapplikasjon
├── DNS
├── database
└── nettverk
```

Hvis databasen slutter å fungere, kan webapplikasjonen slutte å fungere selv om selve webserveren fremdeles kjører.

NDLA viser blant annet hvordan tjenester i større løsninger samarbeider og kan være avhengige av hverandre.

**Les mer:**

* [NDLA – Mikrotjenester](https://ndla.no/en/r/driftsstotte-im-itk-vg2/mikrotjenester/129625ffae)
* [NDLA – Forskjellige typer skytjenester](https://ndla.no/r/driftsstotte-im-itk-vg2/forskjellige-typer-skytjenester/406e35111a)

> **Kort sagt:** En avhengighet beskriver **hva som må fungere for at noe annet skal fungere**.

---

## Hvordan delene henger sammen

Når du dokumenterer en komponent, prøver du egentlig å svare på en serie spørsmål:

| Spørsmål                              | Felt                 |
| ------------------------------------- | -------------------- |
| Hvilken komponent er dette?           | Navn eller ID        |
| Hva er den?                           | Type                 |
| Hva gjør den?                         | Rolle                |
| Hvilket produkt er det?               | Modell               |
| Hvilken programvare styrer maskinen?  | Operativsystem       |
| Hvor befinner den seg?                | Plassering           |
| Hvordan er den koblet til nettverket? | Nettverksinformasjon |
| Hvilke tjenester leverer den?         | Tjenester            |
| Hva er den koblet til?                | Relasjoner           |
| Hva trenger den for å fungere?        | Avhengigheter        |
| Hva bør vi ellers vite?               | Merknad              |

Dette kan uttrykkes som:

```text
Komponent
│
├── identitet
│   ├── navn eller ID
│   └── plassering
│
├── egenskaper
│   ├── type
│   ├── modell
│   └── operativsystem
│
├── funksjon
│   ├── rolle
│   └── tjenester
│
├── nettverk
│   ├── grensesnitt
│   ├── MAC-adresse
│   ├── IP-adresse
│   ├── subnett/prefiks
│   ├── VLAN
│   ├── gateway
│   ├── DHCP
│   └── DNS
│
└── sammenheng
    ├── relasjoner
    ├── avhengigheter
    └── merknader
```

> **Kort sagt:** God systemdokumentasjon beskriver både **delene, egenskapene deres og sammenhengene mellom dem**.

---

## Eksempel på en dokumentert komponent

Verdiene nedenfor er oppdiktet og skal erstattes med bekreftede opplysninger fra IT-laben.

```text
PC-01
├── type: klient
├── rolle: arbeidsstasjon
├── modell: Eksempelmodell 1000
├── operativsystem: Windows 11
├── plassering: stasjon 12
└── nettverk:
    ├── grensesnitt: Ethernet
    ├── MAC-adresse: 02:00:00:00:00:25
    ├── IP-adresse: 192.0.2.25/24
    ├── VLAN: eksempel
    ├── gateway: 192.0.2.1
    └── DNS-server: 192.0.2.10
```

Den samme komponenten kan beskrives gjennom relasjoner:

```text
PC-01 er en klient.
PC-01 har rollen arbeidsstasjon.
PC-01 er koblet til SW-01.
PC-01 tilhører et avtalt VLAN.
PC-01 bruker RTR-01 som standard gateway.
PC-01 bruker DNS-01.
```

Det gir oss fire sentrale spørsmål når vi undersøker et IT-system:

> **Hva er komponenten?**
> **Hva gjør den?**
> **Hvilke egenskaper har den?**
> **Hvordan henger den sammen med resten av systemet?**
