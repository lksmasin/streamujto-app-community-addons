# 🧩 KELP – Komunitní doplňky úložišť

Oficiální repozitář komunitních doplňků (addonů) pro aplikaci [KELP](https://github.com/lksmasin/streamujto-app).

🌐 **[Procházet doplňky online →](https://lksmasin.github.io/streamujto-app-community-addons/)**

> **⚠️ Právní upozornění:** Aplikace KELP neobsahuje žádný obsah ani přístup k žádnému úložišti. Doplňky jsou vytvořeny komunitou a vývojář aplikace za ně nenese žádnou zodpovědnost. Použití doplňků je na vlastní odpovědnost uživatele.

---

## 📦 Dostupné doplňky

| Doplněk | Popis | Auth | Stav |
|---------|-------|------|------|
| [internet-archive](addons/internet-archive/) | Internet Archive – volné filmy (Public Domain) | ❌ Žádná | ✅ Funkční |

---

## 🚀 Jak nainstalovat doplněk

### Způsob 1: Import z URL (doporučeno)

1. Otevřete KELP → **Nastavení** → **Doplňky úložišť**
2. Klepněte na **+ Přidat**
3. Vyberte **Zadat URL adresu**
4. Vložte raw URL doplňku, např.:
   ```
   https://raw.githubusercontent.com/lksmasin/streamujto-app-community-addons/main/addons/internet-archive/internet-archive.json
   ```
5. Potvrďte import

### Způsob 2: Import ze souboru

1. Stáhněte si `.json` soubor doplňku
2. Otevřete KELP → **Nastavení** → **Doplňky úložišť**
3. Klepněte na **+ Přidat** → **Vybrat ze souboru**
4. Vyberte stažený JSON soubor

---

## 📝 Jak přispět

Chcete vytvořit vlastní doplněk? Přečtěte si:

- 📖 [CONTRIBUTING.md](CONTRIBUTING.md) – pravidla pro přispěvatele
- 📚 [Dokumentace addon systému](https://kelp.page/addon-docs.html) – kompletní referenční příručka

### Stručně

1. Forkněte tento repozitář
2. Vytvořte složku `addons/nazev-addonu/`
3. Přidejte `nazev-addonu.json` a `README.md`
4. Otevřete Pull Request

---

## 📂 Struktura repozitáře

```
addons/
├── internet-archive/
│   ├── internet-archive.json
│   └── README.md
├── dalsi-addon/
│   ├── dalsi-addon.json
│   └── README.md
└── ...
```

Každý doplněk má vlastní složku, jejíž název **musí odpovídat** hodnotě `manifest.id` v JSON souboru.

---

## ⚖️ Licence a odpovědnost

- Doplňky v tomto repozitáři jsou poskytovány „tak jak jsou" bez jakékoli záruky.
- Každý uživatel je plně odpovědný za dodržování platných zákonů své země, zejména v oblasti autorských práv.
- Vývojář aplikace KELP neposkytuje, neschvaluje ani nekontroluje žádné doplňky.
- Přispěvatelé jsou odpovědní za obsah svých doplňků.

---

<p align="center">
  <sub>Vytvořeno komunitou pro komunitu • KELP © 2025–2026</sub>
</p>
