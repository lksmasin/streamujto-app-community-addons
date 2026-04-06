# Jak přispět do StreamujTo Community Addons

Děkujeme za zájem o přispění! Tento dokument popisuje pravidla a postup pro přidání nového doplňku.

---

## 📋 Požadavky na doplněk

### Povinné

- [x] Validní JSON soubor podle [dokumentace addon systému](https://lksmasin.github.io/streamujto-app-website/addon-docs.html)
- [x] Povinné sekce: `manifest`, `search`, `streamUrl`
- [x] Unikátní `manifest.id` (kebab-case, bez mezer a diakritiky)
- [x] README.md s popisem doplňku
- [x] Testováno v aplikaci StreamujTo

### Doporučené

- [ ] Vyplněný `manifest.description` a `manifest.author`
- [ ] `manifest.homeUrl` odkazující na domovskou stránku služby
- [ ] Changelog v README.md

---

## 📂 Struktura složky doplňku

```
addons/
└── nazev-addonu/           ← název = manifest.id
    ├── nazev-addonu.json   ← definice doplňku
    └── README.md           ← popis, požadavky, changelog
```

### Příklad README.md pro doplněk

```markdown
# Název Doplňku

Krátký popis, co doplněk dělá a jakou službu propojuje.

## Požadavky

- Účet na example.com (registrace: https://example.com/register)
- VIP / Premium účet (volitelné)

## Instalace

Import URL:
\```
https://raw.githubusercontent.com/lksmasin/streamujto-app-community-addons/main/addons/nazev-addonu/nazev-addonu.json
\```

## Changelog

### 1.0.0
- Počáteční vydání
```

---

## 🔧 Postup přispění

1. **Forkněte** tento repozitář
2. Vytvořte novou větev: `git checkout -b addon/nazev-addonu`
3. Vytvořte složku `addons/nazev-addonu/`
4. Přidejte JSON soubor a README.md
5. **Otestujte** doplněk v aplikaci StreamujTo (import z lokálního souboru)
6. Commitněte: `git commit -m "Add nazev-addonu addon"`
7. Pushněte a otevřete **Pull Request**

---

## ✅ Kontrolní seznam před PR

Před odesláním Pull Requestu ověřte:

- [ ] JSON soubor je validní (žádné trailing commas, správné uvozovky)
- [ ] `manifest.id` odpovídá názvu složky
- [ ] Doplněk funguje v aplikaci (login, vyhledávání, přehrávání)
- [ ] README.md obsahuje popis a instalační URL
- [ ] Neexistuje doplněk se stejným `manifest.id`

---

## 🚫 Co nebude přijato

- Doplňky s duplicitním `manifest.id`
- Nefunkční doplňky (nevalidní JSON, nefungující endpointy)
- Doplňky bez README.md
- Doplňky porušující pravidla GitHubu

---

## 📝 Validace JSON

CI automaticky ověří při každém PR:

1. JSON soubor je syntakticky validní
2. Obsahuje povinné klíče: `manifest.id`, `manifest.name`, `search`, `streamUrl`
3. `manifest.id` odpovídá názvu složky

---

## ❓ Otázky?

Pokud máte dotazy nebo potřebujete pomoc s tvorbou doplňku:

- 📚 [Dokumentace addon systému](https://lksmasin.github.io/streamujto-app-website/addon-docs.html)
- 💬 [Discord server](https://discord.gg/your-invite-code)
- 🐛 [Issues](https://github.com/lksmasin/streamujto-app-community-addons/issues)
