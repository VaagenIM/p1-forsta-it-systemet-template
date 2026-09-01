# Git i terminalen, GitHub Desktop og VS Code

Git registrerer endringer i elevrepoet. Du lærer kommandoene i terminalen først. Når du forstår arbeidsflyten, kan du bruke GitHub Desktop eller kildekontrollvisningen i VS Code som grafisk støtte.

## Første gang

1. Åpne Classroom50-invitasjonen i Teams-kanalen og opprett ditt elevrepo.
2. Åpne elevrepoet på GitHub og kopier adressen fra **Code**.
3. Åpne terminalen i mappen der du vil lagre elevrepoet.
4. Klon elevrepoet og gå inn i mappen:

```bash
git clone <adresse-til-elevrepo>
cd <navn-på-repomappen>
```

5. Kontroller at du er i riktig elevrepo:

```bash
git status
```

6. Åpne mappen i VS Code. Hvis kommandoen er tilgjengelig, kan du bruke:

```bash
code .
```

Kontroller at mappen inneholder `README.md`, `plan/`, `ressurser/` og `arbeid/`.

## Registrer og send en endring

Lagre filen i VS Code. Kjør deretter kommandoene i terminalen fra repomappen:

```bash
git status
git diff
git add <filsti>
git diff --staged
git commit -m "docs: beskriv endringen kort"
git push
```

| Kommando | Hva du kontrollerer |
|---|---|
| `git status` | hvilke filer som er endret, og hva som er valgt for registrering |
| `git diff` | innholdet som er endret, men ikke valgt |
| `git add <filsti>` | velger én bestemt fil til neste registrering |
| `git diff --staged` | innholdet som blir med i neste registrering |
| `git commit -m "..."` | registrerer det valgte arbeidssteget lokalt |
| `git push` | sender de registrerte endringene til GitHub |

Åpne elevrepoet på GitHub etter `git push`, og kontroller at den siste endringen vises.

## Gode registreringsmeldinger

Beskriv hva som faktisk ble endret:

```text
docs: legg til klient i komponentoversikten
docs: oppdater fysisk topologi
fix: rett IP-adresse i komponentoversikten
```

Registrer én meningsfull endring om gangen. Ikke bruk `git push --force`.

## Bruk GitHub Desktop etter terminalen

Når du kan terminalflyten, kan du gjøre den samme arbeidsflyten i GitHub Desktop:

1. Åpne elevrepoet i GitHub Desktop.
2. Velg **Changes** og kontroller hvilke filer og linjer som er endret.
3. Merk bare filene som skal være med i den aktuelle registreringen.
4. Skriv en kort registreringsmelding i **Summary**.
5. Velg **Commit to main**, eller tilsvarende knapp for grenen du arbeider på.
6. Velg **Push origin** for å sende registreringen til GitHub.
7. Åpne elevrepoet på GitHub og kontroller at endringen vises.

Hvis elevrepoet ikke allerede finnes lokalt, kan du velge **File -> Clone Repository**, finne elevrepoet eller lime inn adressen under **URL**, velge lokal mappe og trykke **Clone**.

| GitHub Desktop | Tilsvarende terminalsteg |
|---|---|
| **Changes** og visning av forskjeller | `git status` og `git diff` |
| merkede filer | `git add <filsti>` |
| **Commit to main** eller tilsvarende | `git commit` |
| **Push origin** | `git push` |

## Gradvis bruk av VS Code

Når du kan terminalflyten, kan du bruke **kildekontroll (Source Control)** i VS Code til å:

1. se endrede filer og forskjeller
2. velge filer for registrering
3. skrive registreringsmelding og registrere endringen
4. synkronisere eller sende endringen til GitHub

Kommandoene i tabellen over er fortsatt referansen når du skal forstå hva GitHub Desktop og VS Code gjør.

Hjelp: [Git-dokumentasjon](https://git-scm.com/docs), [kom i gang med GitHub Desktop](https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop) og [kildekontroll i VS Code](https://code.visualstudio.com/docs/sourcecontrol/quickstart).

## Hvis noe ikke virker

- **`not a git repository`:** Gå til mappen som inneholder `README.md`, og kjør `git status` på nytt.
- **Ingen endringer vises:** Kontroller at filen er lagret, og at du redigerer filen i riktig elevrepo.
- **`nothing to commit`:** Det er ingen nye valgte endringer. Kjør `git status` og `git diff`.
- **Pålogging eller sending mislykkes:** Kontroller GitHub-kontoen og vis feilmeldingen til læreren uten å dele passord eller tilgangstegn.
