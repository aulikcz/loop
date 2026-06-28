# Tales from the Loop — Character Sheets

Webová aplikace pro správu postav z RPG Tales from the Loop.  
Postavy se ukládají jako JSON soubory přímo do tohoto repozitáře. DM i hráči vždy otevírají **stejnou URL** — žádné posílání nových odkazů.

---

## Rychlý start

### 1. Vytvoř repozitář

Na GitHubu vytvoř nový **veřejný** repozitář (např. `tftl-characters`).  
Uploadni soubor `index.html` do kořene.

### 2. Zapni GitHub Pages

`Settings → Pages → Source: Deploy from branch → branch: main, folder: / (root) → Save`

Stránka bude dostupná na adrese:  
`https://{tvůj-username}.github.io/{název-repozitáře}/`

### 3. Vytvoř Personal Access Token

1. Jdi na [github.com/settings/tokens?type=beta](https://github.com/settings/tokens?type=beta)
2. Klikni **Generate new token**
3. Pojmenuj ho (např. `tftl-sheet`)
4. Pod **Repository access** vyber jen tento repozitář
5. Pod **Permissions → Contents** nastav **Read and Write**
6. Klikni **Generate token** a zkopíruj ho

### 4. Nastav aplikaci

Na stránce klikni na **⚙** (Nastavení) a vyplň:
- GitHub Owner: tvůj username
- Název repozitáře: název repa
- Větev: `main`
- Token: vložte zkopírovaný token

Token se uloží do `localStorage` prohlížeče (nikam se neodesílá).

---

## Používání

| Akce | Jak |
|------|-----|
| **Načíst postavu** | Vyber z rozbalovacího menu |
| **Nová postava** | Klikni na **+ Nová** |
| **Uložit** | Klikni **💾 Uložit** nebo `Ctrl+S` |
| **Atributy** | Klikni na tečky (1–5) |
| **Dovednosti** | Klikni na tečky, druhý klik na stejnou ruší |
| **Luck Points** | Klikni na bublinu pro označení jako použitou |
| **XP** | Klikni na čtverečky |

---

## Struktura souborů

```
/
├── index.html          # celá aplikace
└── characters/
    ├── anna.json       # každá postava = jeden JSON
    ├── jerry.json
    └── ...
```

---

## Sdílení s hráči

Každý hráč navštíví stejnou URL. Při prvním použití si nastaví token ve svém prohlížeči.  
Alternativně: DM má token a upravuje postavy za hráče.

---

## Bezpečnost

- Token je uložen jen v localStorage daného prohlížeče
- Pro maximální bezpečnost použij Fine-grained token omezený jen na tento repozitář
- Repo může být veřejné (kód stránky) i soukromé (pak GitHub Pages vyžaduje plán Pro)
