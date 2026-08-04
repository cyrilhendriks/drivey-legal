# CLAUDE.md — Drivie Legal & Support

Twee statische pagina's, gehost via GitHub Pages op
`https://cyrilhendriks.github.io/drivey-legal/` — geen build, geen
framework, geen dependencies. Een push naar `main` is live binnen enkele
minuten, zonder review-stap.

## Wat hier staat

- **`index.html`** — Privacy & Juridisch: trademark-disclaimer
  (Homey/Athom), privacybeleid, aankopen/updates/onafhankelijke
  ontwikkelaar-clausule, aansprakelijkheid. Nederlands is het officiële
  origineel (zie de footer op de pagina zelf); de Engelse tekst eronder is
  een vertaling, louter ter informatie.
- **`support.html`** — contactformulier (Web3Forms) + FAQ.

## Verband met de apps

De tekst in `index.html` wordt **ook** losstaand gereproduceerd in de apps
zelf, als platte tekst (geen link, geen webview):
`cyrilhendriks/drivey` → `App/Sources/Settings/LegalView.swift`,
`cyrilhendriks/drivey-android` → het Kotlin-equivalent. Wijzig je de
juridische tekst hier inhoudelijk, werk die twee bestanden dan in dezelfde
ronde bij — anders lopen de in-app-tekst en de publieke pagina uiteen.

Deze URL (`.../drivey-legal/`) is ook de **Privacy Policy URL** en de
verwijzing achter de "Terms of Use / EULA"-link in beide apps' paywalls en
in de App Store/Play Store-omschrijvingen — een inhoudelijke wijziging hier
kan dus rechtstreeks App Review-consequenties hebben (zie
`cyrilhendriks/drivey` → `docs/agents/publishing.md`).

## Harde regels

1. **Wijzigingen aan de juridische tekst (`index.html`) via een PR, niet
   rechtstreeks op `main`** — zonder build of CI-check hier is de PR de
   enige controle vóór het live staat. `support.html` (contactformulier,
   FAQ, styling) mag met minder ceremonie, naar inzicht.
2. **Nederlands blijft het officiële origineel.** Wijzig je de
   Nederlandse tekst, werk de Engelse vertaling in dezelfde wijziging bij.
3. **Geen secrets nodig.** Het contactformulier praat rechtstreeks met
   Web3Forms vanuit de browser; er is geen server, geen API-key in deze
   repo.
