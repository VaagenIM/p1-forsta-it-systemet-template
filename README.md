# Periode 1 – Forstå IT-systemet

I denne perioden skal du undersøke og dokumentere **hele IT-laben** slik at en annen elev kan forstå hva systemet består av, hvordan delene er koblet sammen og hvilke avhengigheter systemet har.

Du begynner ved **egen stasjon**: klienten, kablene og den nærmeste nettverkstilkoblingen. Derfra følger du forbindelsene videre til den delte infrastrukturen, nettverkstjenestene, serverne og de virtuelle ressursene i IT-laben. Stasjonen er startpunktet for undersøkelsen, ikke hele systemgrensen.

Du dokumenterer systemets **arkitektur**. **Infrastrukturen** er det tekniske grunnlaget du undersøker, mens **topologien** viser hvordan komponentene er plassert og koblet sammen.

**Classroom50-invitasjon:** Lenken publiseres i Teams-kanalen.

## Før du begynner

- [ ] Jeg er logget inn på riktig GitHub-konto.
- [ ] Jeg har åpnet Classroom50-invitasjonen i Teams og opprettet mitt eget elevrepo.
- [ ] Jeg har klonet elevrepoet med Git i terminalen og åpnet mappen i VS Code.
- [ ] Jeg kan lagre en fil og kontrollere endringen med Git i terminalen.
- [ ] Jeg kan åpne diagrams.net og en `.drawio`-fil.
- [ ] Jeg har deltatt i dagens muntlige gjennomgang.

Hvis noe mangler, bruk [programvare- og verktøyoversikten](ressurser/programvare.md) og delen [Hvis du står fast](#hvis-du-står-fast) før du fortsetter.

## Start her

1. Les [periodeplanen](plan/periodeplan.md) første gang du åpner elevrepoet.
2. Åpne planen for [uke 36](plan/uke-36.md), [uke 37](plan/uke-37.md) eller [uke 38](plan/uke-38.md).
3. Gjør arbeidssteget som står for dagen.
4. Åpne fagstoffet og verktøyhjelpen som står rett under arbeidssteget.
5. Fortsett i arbeidsfilen ukeplanen peker til.
6. Bruk ukeskontrollen før du avslutter arbeidet.

## Slik arbeider du hver undervisningsdag

Hver dag følger den samme rytmen:

1. **Dagens tema:** Finn ut hva du skal forstå eller lære.
2. **Dagens arbeid:** Følg arbeidssteget og bruk fagstoffet som står rett under.
3. **Arbeidskø:** Gjør punktene i rekkefølge. Fortsett der du stoppet hvis noe gjenstår.
4. **Dagens endring:** Kontroller at du kan vise en konkret endring i en arbeidsfil, et diagram eller Git-historikken.
5. **Neste steg:** Les hva dagens arbeid forbereder deg på.

På fredag bruker du ukeskontrollen til å se hva som er gjort, hva som fungerer, hva som er dokumentert og hva som må forbedres.

## Min systemdokumentasjon

Oppdater bare punktene nedenfor i denne delen av `README.md`. Bruk avtalte systemnavn og ikke skriv personopplysninger eller hemmeligheter.

- **Kort systembeskrivelse:**
- **Startpunkt i IT-laben:**
- **Viktigste dokumentasjonslenke:** [Systemoversikt](arbeid/arkitektur/oversikt.md)

## Les først

- [Periodeplan og ukeplaner](plan/periodeplan.md)
- [Språk- og dokumentasjonskonvensjoner](ressurser/konvensjoner.md)
- [Slik vurderes arbeidet](plan/vurdering.md)

## Bruk når ukeplanen peker hit

- [NDLA-fagstoff for alle begreper og temaer](ressurser/ndla-fagstoff.md)
- [Programvare og verktøy](ressurser/programvare.md)
- [Git i terminalen, GitHub Desktop og VS Code](ressurser/git.md)
- [Etiketter i topologidiagrammer](ressurser/diagrametiketter.md)
- [Nettverkskjeden](ressurser/nettverkskjeden.md)
- [IP-adresse, subnett og standard gateway](ressurser/ip-og-subnett.md)
- [Nettverkskommandoer](ressurser/nettverkskommandoer.md)
- [Følg stasjonen i UniFi Network](ressurser/unifi-network.md)
- [Finn virtuell og fysisk infrastruktur i Proxmox VE](ressurser/proxmox-ve.md)
- [Linux-konsoll i Proxmox](ressurser/linux-konsoll.md)
- [Test en tjeneste](ressurser/tjenestetest.md)
- [Feilsøkingsmetode](ressurser/feilsoking.md)

## Oppslag ved behov

- [Begreper i komponentoversikten](ressurser/begreper-i-komponentoversikten.md)
- [Velg riktig kilde](ressurser/kilder.md)
- [Eksempler](ressurser/eksempler.md)

## Dette skal du dokumentere

- [Komponentoversikt](arbeid/komponentoversikt.md)
- [Systemoversikt](arbeid/arkitektur/oversikt.md)
- [Fysisk topologi](arbeid/arkitektur/diagrammer/fysisk-topologi.drawio)
- [Logisk topologi](arbeid/arkitektur/diagrammer/logisk-topologi.drawio)
- [Fysisk topologi – forhåndsvisning](arbeid/arkitektur/diagrammer/fysisk-topologi.svg)
- [Logisk topologi – forhåndsvisning](arbeid/arkitektur/diagrammer/logisk-topologi.svg)
- [Problemer og løsninger](arbeid/feilsoking.md)
- [Egen kildeliste](arbeid/kildeliste.md)

## Struktur

```text
forsta-it-systemet/
├── README.md
├── plan/                    # hva som skal skje og når
├── ressurser/               # fagstoff, verktøy, konvensjoner og eksempler
└── arbeid/                  # arbeidsproduktene du skal utvikle
    ├── komponentoversikt.md
    ├── feilsoking.md
    ├── kildeliste.md
    └── arkitektur/
        ├── oversikt.md
        └── diagrammer/
            ├── fysisk-topologi.drawio
            ├── fysisk-topologi.svg
            ├── logisk-topologi.drawio
            └── logisk-topologi.svg
```

Du skal endre delen `Min systemdokumentasjon` i `README.md` og filene under `arbeid/`. Planene og ressursene brukes som arbeidsgrunnlag.

## Arbeidsmåte

**undersøke -> forstå -> gjøre -> teste/feilsøke -> dokumentere -> vurdere**

Bruk versjonskontroll (version control) med Git underveis. Kontroller endringene og registrer små, sammenhengende arbeidssteg med `git commit`.

Lær først arbeidsflyten i terminalen. Deretter kan du bruke GitHub Desktop eller VS Code til de samme Git-stegene.

Eksempler:

```text
docs: legg til fysisk server i komponentoversikten
docs: oppdater fysisk nettverksdiagram
docs: dokumenter DHCP og standard gateway
fix: rett feil IP-adresse i komponentoversikten
```

## Regler

- Skriv for en leser som ikke kjenner systemet fra før.
- Følg [konvensjonene](ressurser/konvensjoner.md).
- Ikke kopier samme informasjon flere steder; lenk til detaljene.
- Oppdater dokumentasjonen når systemet eller forståelsen din endres.
- Ikke legg inn passord, API-nøkler, personopplysninger eller andre hemmeligheter.

## Ferdig når

- [ ] delen `Min systemdokumentasjon` i `README.md` er oppdatert
- [ ] [komponentoversikten](arbeid/komponentoversikt.md) beskriver hele IT-laben med utgangspunkt i egen stasjon
- [ ] fysisk og logisk topologi følger forbindelsene fra egen stasjon til den delte infrastrukturen og tjenestene
- [ ] diagrammene bruker samme ID-er som komponentoversikten og har ingen plassholdere eller generiske startnavn
- [ ] begge topologiene er eksportert som `.svg` og kan vises direkte på GitHub
- [ ] [systemoversikten](arbeid/arkitektur/oversikt.md) forklarer sammenhengene i hele IT-laben
- [ ] minst ett problem eller én feil er dokumentert med løsning og kontroll
- [ ] [kildelisten](arbeid/kildeliste.md) viser hvilke kilder som faktisk er brukt
- [ ] Git-historikken viser små, beskrivende endringer
- [ ] en medelev kan bruke dokumentasjonen til å følge systemet fra én stasjon og videre gjennom hele IT-laben

## Levering

**Frist:** fredag 18. september 2026.

1. Fullfør [sluttkontrollen for uke 38](plan/uke-38.md#sluttkontroll).
2. Kontroller hvilke filer som er endret.
3. Eksporter de oppdaterte diagrammene som `.svg`.
4. Registrer den siste meningsfulle endringen med `git commit` eller **Commit** i GitHub Desktop eller VS Code.
5. Send endringene til GitHub med `git push` eller **Push origin**.
6. Åpne elevrepoet på GitHub og kontroller at siste endring og SVG-diagrammene vises.
7. Kontroller at det ferdig leverte repoet viser din individuelle systemforklaring.

## Hvis du står fast

1. Finn dagens arbeidssteg og ukens kontrollpunkt.
2. Sammenlign med [eksemplene](ressurser/eksempler.md).
3. Åpne fagstoffet eller verktøyhjelpen som står ved arbeidssteget.
4. Noter hva du prøvde og hva som skjedde.
5. Be om veiledning med ett konkret spørsmål.

Hvis et verktøy eller en labressurs ikke er tilgjengelig, skal du ikke gjette. Dokumenter kort hva som mangler, og fortsett med fagstoffet eller en annen avtalt del av arbeidet.
