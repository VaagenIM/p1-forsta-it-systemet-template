# NDLA-fagstoff for perioden

## System, dokumentasjon og arbeidsmåte

| Begreper og tema | NDLA-fagstoff | Dette skal du finne ut |
|---|---|---|
| IT-system, arkitektur, infrastruktur, komponent, avhengighet, komponentoversikt, fysisk topologi og logisk topologi | [Hva bør du dokumentere i IT-systemer – Vg1](https://ndla.no/r/konseptutvikling-og-programmering-im-ikm-vg1/hva-bor-du-dokumentere-i-it-systemer/b9c7e4c0b0) | Finn hva en systembeskrivelse og et nettverkskart bør vise. Bruk definisjonene av arkitektur, infrastruktur og topologi i [periodeplanen](../plan/periodeplan.md). |
| Klient, server og tjeneste | [Klargjøre maskin til å brukes som server – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/klargjore-maskin-til-a-brukes-som-server/14e705c5ae) og [nettverkstjenester og protokoller – Vg2](https://ndla.no/e/driftsstotte-im-itk-vg2/nettverkstjenester-og-protokoller/d4b104e3ab) | Skill maskinen fra rollen den har, og forklar hvilken tjeneste klienten bruker. |
| Operativsystem | [Operativsystem – Vg1](https://ndla.no/nb/r/teknologiforstaelse-im-ikm-vg1/operativsystem/c04d611412) | Forklar hvordan operativsystemet styrer maskinressurser og programmer. |
| Linux på vert og gjest | [Operativsystem – Vg1](https://ndla.no/nb/r/teknologiforstaelse-im-ikm-vg1/operativsystem/c04d611412) | Skill systemet som kjører på Proxmox-verten fra Linux-systemet i en VM eller container. Bruk [Linux-konsoll i Proxmox](linux-konsoll.md) ved praktisk arbeid. |
| Dokumentasjon av problemer og løsninger | [Feilsøkingsmetodikk – Vg1](https://ndla.no/r/teknologiforstaelse-im-ikm-vg1/feilsokingsmetodikk/ad89a52950) | Bruk særlig punkt 7: dokumenter feilen, årsaken og løsningen. |
| Feilsøking av nettverk og maskin | [Feilsøking på nettverk og maskin – Vg1](https://ndla.no/nb/r/teknologiforstaelse-im-ikm-vg1/feilsoking-pa-nettverk-og-maskin/c1b1b6defb) | Avgrens feilen fra fysisk forbindelse til program eller tjeneste. |
| Repo, versjonskontroll og `git commit` | [Viktige nettsteder for programmering – NDLA, Elektro Vg1](https://ndla.no/r/elektroniske-kretser-og-nettverk-el-ele-vg1/viktige-nettsteder-for-programmering/df30d2d199) | Forklar hvorfor Git brukes, og registrer endringene dine som beskrevet i [Git i terminalen, GitHub Desktop og VS Code](git.md). |

## Maskinvare

| Begreper og tema | NDLA-fagstoff | Dette skal du finne ut |
|---|---|---|
| Datamaskin, komponent, hovedkort, prosessor (CPU), arbeidsminne (RAM), lagring, porter og nettverkskort | [Datamaskinens komponenter – Vg1](https://ndla.no/e/teknologiforstaelse-im-ikm-vg1/datamaskinens-komponenter/dbd8bc410a) | Finn og navngi de fysiske hovedkomponentene. |
| Prosessor (CPU) | [Prosessoren – Vg1](https://ndla.no/r/teknologiforstaelse-im-ikm-vg1/prosessoren/d589269a21) | Forklar prosessorens rolle og forbindelsen til de andre komponentene. |
| Hovedkort og tilkoblinger | [Hovedkortet – Vg1](https://ndla.no/nb/r/teknologiforstaelse-im-ikm-vg1/hovedkortet/5acc026e45) | Finn hvordan hovedkortet kobler sammen komponentene. |
| Arbeidsminne (RAM) og lagring | [Minnehierarki – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/minnehierarki/6fbc22ea30) og [lagringsenheter – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/lagringsenheter/d8bd4af7c5) | Skill flyktig arbeidsminne fra varig lagring. |

## Nettverk

| Begreper og tema | NDLA-fagstoff | Dette skal du finne ut |
|---|---|---|
| Nettverkskort, kabel, port, aksesspunkt, svitsj og ruter | [Komponentene i datanettverk – Vg2](https://ndla.no/e/driftsstotte-im-itk-vg2/komponentene-i-datanettverk/6acd26e59c) | Identifiser komponentene og rollen deres før de tegnes. |
| Dream Router og Flex Mini ved stasjonen | [Komponentene i datanettverk – Vg2](https://ndla.no/e/driftsstotte-im-itk-vg2/komponentene-i-datanettverk/6acd26e59c) | Bruk [UniFi-ressursen](unifi-network.md) til å skille gateway, svitsj, port og nett i det konkrete utstyret. |
| Ethernet, MAC-adresse og ARP | [5-lags TCP/IP-modell – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/5-lags-tcpip-modell/9e31c212f6) og [svitsj – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/svitsj/a33b4b015c) | Plasser Ethernet og ARP på datalinklaget og forklar hvordan svitsjen bruker MAC-adresser. |
| IP-adresse, subnettmaske eller prefiks | [IP-adresser – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/ip-adresser/3082395965) | Skill nettverksdel fra vertsdel og avgjør hva som er lokalt. |
| Ruter og standard gateway | [Ruter – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/ruter/eb2ce6553f) | Forklar hvordan trafikk sendes mellom nettverk. |
| DHCP | [DHCP – Vg2](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dhcp/8755440e02) | Finn hvordan klienten får IP-adresse, subnettmaske, gateway og DNS-adresse. |
| DNS | [DNS-oppslag – Vg2](https://ndla.no/nb/r/driftsstotte-im-itk-vg2/dns-oppslag/8b81c28535) | Følg oversettelsen fra domenenavn til IP-adresse. |
| Tjeneste, protokoll og port | [Nettverkstjenester og protokoller – Vg2](https://ndla.no/e/driftsstotte-im-itk-vg2/nettverkstjenester-og-protokoller/d4b104e3ab) | Knytt klientens behov til riktig tjeneste og protokoll. |
| Virtuelt lokalnettverk (VLAN) | [Virtuelt lokalnettverk (VLAN) – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelt-lokalnettverk-vlan/9d865afa88) | Skill fysisk nettverksutstyr fra logisk segmentering. |

## Virtualisering

| Begreper og tema | NDLA-fagstoff | Dette skal du finne ut |
|---|---|---|
| Fysisk og virtuell infrastruktur, vertsmaskin, hypervisor og virtuell maskin (VM) | [Virtuelle maskiner – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelle-maskiner/b8a976125b) | Følg avhengigheten fra fysisk vert gjennom hypervisoren til den virtuelle maskinen. |
| Virtuelt nettverkskort og virtuell svitsj | [Virtuelle maskiner – Vg2](https://ndla.no/r/driftsstotte-im-itk-vg2/virtuelle-maskiner/b8a976125b) | Koble den virtuelle maskinen til den logiske og fysiske topologien. |
