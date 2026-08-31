# Programvare og verktøy

Bruk verktøyet som arbeidssteget peker til. Les fagstoffet først, åpne deretter verktøyet og dokumenter bare opplysninger som er relevante for IT-laben.

## VS Code og Markdown

**Brukes til:** å lese planer, redigere arbeidsfiler, følge relative lenker og kontrollere hva som er endret.

**Du skal kunne:**

1. åpne hele elevrepoet som mappe i VS Code
2. finne riktig fil fra `README.md`
3. redigere og lagre Markdown
4. åpne forhåndsvisningen og kontrollere overskrifter, tabeller og lenker

Hjelp: [Markdown i Visual Studio Code](https://code.visualstudio.com/docs/languages/markdown).

## Git og versjonskontroll

**Brukes til:** å kontrollere og registrere små, sammenhengende endringer i dokumentasjonen.

Du lærer først arbeidsflyten i terminalen: `git status`, `git diff`, `git add`, `git commit` og `git push`. Deretter kan du gradvis bruke GitHub Desktop eller kildekontrollvisningen i VS Code for å se forskjeller, velge filer, registrere endringer og sende dem til GitHub.

Følg [Git i terminalen, GitHub Desktop og VS Code](git.md) første gang og når du står fast.

## diagrams.net

**Brukes til:** å tegne fysisk og logisk topologi.

**Du skal kunne:**

1. åpne en eksisterende `.drawio`-fil
2. plassere og navngi komponenter og tegne forbindelser
3. lagre kildefilen som `.drawio`
4. eksportere samme diagram som `.svg` med samme grunnnavn
5. kontrollere etikettene etter [standarden for topologidiagrammer](diagrametiketter.md)
6. åpne SVG-filen og kontrollere at tekst og forbindelser er lesbare

Hjelp: [Innføring i diagrams.net-editoren](https://www.drawio.com/docs/getting-started/).

## Terminal og nettverkskommandoer

Bruk [nettverkskommandoer](nettverkskommandoer.md) for Windows-klienten og Linux i Proxmox-konsollen. Der finner du kommando, eksempel, tolkning og kilde ved arbeidssteget.

## UniFi Network

**Brukes til:** å følge klienten ved stasjonen videre til Flex Mini, Dream Router, nett og standard gateway og derfra forstå den delte infrastrukturen i IT-laben.

Start med klienten ved egen stasjon. Kontroller opplysningene mot den fysiske forbindelsen og utvid deretter dokumentasjonen til resten av IT-laben. Ikke endre porter, VLAN, nettverk, trådløse innstillinger eller enhetskonfigurasjon.

Følg den elevrettede framgangsmåten i [UniFi Network](unifi-network.md). Der ligger også offisiell dokumentasjon for Dream Router og Flex Mini.

## Proxmox VE

**Brukes til:** å finne fysiske noder, virtuelle maskiner, status, tildelte ressurser og nettverkskoblinger i IT-laben.

Finn først den fysiske noden, deretter hypervisoren og de avtalte virtuelle maskinene. Ikke opprett, endre, start, stopp eller slett ressurser med mindre oppgaven ber om det.

Følg [Proxmox VE](proxmox-ve.md) for å finne ressursene og [Linux-konsoll](linux-konsoll.md) før du kjører kommandoer i Node Shell eller en VM-/CT-konsoll.

## Nettleser og tjenestetest

**Brukes til:** å åpne NDLA-fagstoff, offisiell dokumentasjon og en avtalt tjeneste i IT-laben.

En nettside som åpnes, er bare belegg for at den aktuelle tjenestetesten lyktes. Bruk resultatene fra nettverkskjeden når du skal forklare hvorfor tjenesten er tilgjengelig.

Følg [test en tjeneste](tjenestetest.md) når arbeidssteget ber deg kontrollere en avtalt tjeneste.

## Sikker bruk

- Ikke legg passord, påloggingstegn, API-nøkler eller personopplysninger i dokumentasjonen.
- Ikke endre felles nettverk, servere eller virtuelle ressurser uten at du får beskjed.
- Stopp og be om veiledning hvis et verktøy viser flere systemer enn oppgaven omtaler, eller hvis du er usikker på systemgrensen.

## Hvis du mangler tilgang

1. Kontroller at du bruker riktig konto, elevrepo eller riktig klient.
2. Noter hvilken side, fil eller tjeneste du prøvde å åpne.
3. Noter feilmeldingen uten å kopiere hemmeligheter eller personopplysninger.
4. Be om veiledning og vis hva du allerede har kontrollert.
5. Fortsett med fagstoff, diagram eller en annen avtalt arbeidsfil mens du venter.
