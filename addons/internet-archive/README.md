# Internet Archive (Public Domain)

Legální doplněk pro vyhledávání a přehrávání volně dostupných filmů z [Internet Archive](https://archive.org) – největší knihovny volně šiřitelného digitálního obsahu na světě.

## O Internet Archive

[Internet Archive](https://archive.org) je nezisková organizace, která archivuje digitální obsah. Sekce **Community Video / Movies** obsahuje tisíce filmů ve veřejném vlastnictví (Public Domain), které je legální sledovat, stahovat i sdílet.

> ℹ️ Veškerý obsah dostupný přes tento doplněk je **legálně šiřitelný** (Public Domain / Creative Commons).

## Požadavky

- **Žádné** – Internet Archive je veřejně přístupný, nepotřebujete účet ani předplatné.

## Funkce

- ✅ Vyhledávání filmů v archivu
- ✅ Přímé streamování souborů
- ✅ Žádná autentizace
- ✅ 100 % legální obsah (Public Domain)

## Instalace

### Import z URL

```
https://raw.githubusercontent.com/lksmasin/streamujto-app-community-addons/main/addons/internet-archive/internet-archive.json
```

1. Otevřete StreamujTo → **Nastavení** → **Doplňky úložišť**
2. Klepněte na **+ Přidat** → **Zadat URL adresu**
3. Vložte URL výše a potvrďte

## Omezení

- Vyhledávání prochází metadata Internet Archive – názvy nemusí vždy odpovídat běžným filmovým názvům.
- Ne všechny položky mají MP4 soubor. Pokud archivní záznam obsahuje pouze jiné formáty (OGV, AVI), streamování nemusí fungovat.
- Kvalita videí se výrazně liší – od SD po HD. Jedná se převážně o historické a nezávislé filmy.

## Technické detaily

| Vlastnost | Hodnota |
|-----------|---------|
| ID | `internet-archive` |
| Typ | `api` (JSON REST API) |
| API | [Internet Archive Advanced Search](https://archive.org/advancedsearch.php) |
| Auth | Žádná |
| Capabilities | `search`, `directStream` |
| Formát výsledků | MP4 (original source) |

## Příklady vyhledávání

- `Night of the Living Dead` – klasický horor (1968)
- `Nosferatu` – německý expresionistický film (1922)
- `The General` – Buster Keaton komedie (1926)
- `Plan 9 from Outer Space` – kultovní sci-fi (1957)

## Changelog

### 1.1.0

- Opraven regex pro extrakci názvu video souboru z metadat (pořadí klíčů `name`/`source` v JSON)
- Přidán fallback regex – pokud neexistuje MP4 se `source: "original"`, použije se jakýkoli MP4
- Název souboru v URL je nyní kódován (`urlencode`) pro správné fungování s mezerami a speciálními znaky

### 1.0.0
- Počáteční verze
- Vyhledávání přes Advanced Search API
- Streamování MP4 souborů z originálních zdrojů
