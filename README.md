# youtube-skill

Prémium **Claude Code skill** magyar YouTube- és oktatóvideók készítéséhez. Egy
nyers ötletből, oktatóanyagból, személyes felismerésből vagy ügyfélhelyzetből
kész **diagnózist, 25 címet, 8 hookot, teljes videóvázat, retenciós tervet,
tükörmondatokat és teleprompter-vázlatot** ad — úgy, hogy a néző a te
történeteden keresztül **saját magára ismerjen**.

A skill alapelve:

> **Nem a saját történetemről beszélek. A néző problémájáról beszélek a saját
> történetemen keresztül.** A néző azt érezze: *„Ez nem róla szól. Ez rólam szól."*

## A skill neve

**`youtube-figyelem-atalakito`** (v3.0.0)

## Mit tud?

Nem csak a Tükör-technikát használja — **teljes technikai rendszert** (45
technika) alkalmaz a címre, a nyitásra, a középrészre, a rehookokra, a zárásra
és a konkrét nyelvi átírásra. Amikor odaadsz neki egy ötletet, mindig egy
kötelező, 17 szekciós csomagot ad vissza, többek között:

1. **Rövid diagnózis** — felszíni téma, valódi konfliktus, kimondatlan érzés, rejtett minta, tét.
2. **A videó valódi témája** — felszíntől a mélyebb emberi igazságig.
3. **Kötelező átírási táblázat** — hogyan lesz a „rólam" mondatból „róla" mondat (min. 8 sor).
4. **5 központi kérdés** + a javasolt.
5. **25 cím** öt csoportban (tabloid, paradoxon, kérdéses, személyes-univerzális, kellemetlen igazság).
6. **A legjobb 1–3 cím** indoklással.
7. **8 hook** különböző technikákkal (sosem „Ebben a videóban…").
8. **Attila-féle videóváz** 8–11 résszel, technikákkal és Ő/Én/Mi ritmussal.
9. **Retenciós terv** másodperc-bontásban.
10. **20+ rehook / visszadobás mondat** a konkrét témára.
11. **15 tükörmondat** a nézői önfelismeréshez.
12. **12 nyelvi formula** (Talán… / Lehet, hogy… / Mi van, ha… / Azt hittem…, de…).
13. **Oktatói tanulságok** (ha oktató a videó).
14. **5 zárás** különböző stílusban.
15. **Rövid teleprompter-vázlat**.
16. **Technikák térképe** — melyik technika hol dolgozik.
17. **Ajánlott végső csomag** — főcím + első 30 mp + szerkezet 5 pontban.

A teljes rendszer a `.claude/skills/youtube-figyelem-atalakito/SKILL.md`-ben van;
kiegészítő technika-katalógusok és egy forgatókönyv-sablon a `references/` és
`assets/` mappákban.

## Hogyan hívd elő?

- Írd be a Claude Code-ban: `/youtube-figyelem-atalakito`, majd add meg az ötletet, **vagy**
- egyszerűen mondd el az ötleted, és kérd, hogy a YouTube-skillel dolgozzon rajta
  (a Claude a leírás alapján magától is előhívja).

Példák:
- „Van egy videóötletem arról, hogy elvesztem az AI-ban — futtasd rá a youtube-figyelem-atalakito skillt."
- „Csinálj címeket, hookot és videóvázat ehhez: el kell mondanom egy ügyfélnek, hogy rossz irányba vittem egy projektet."

A bemenet lehet töredékes vagy beszélt nyelvű — a skill ésszerű feltételezéseket
tesz (és jelöli őket), ha hiányzik valami.

## Telepítés / elérés

### Felhőben (Claude Code on the web)
Semmi teendő. A skill ebben a repóban él (`.claude/skills/`), így amikor ezen a
repón indítasz felhős sessiont, **automatikusan elérhető**. Csak hívd elő.

### Asztali gépen — A opció (ezen a repón belül)
Klónozd a repót, és dolgozz benne — a project-skill automatikusan betöltődik:
```bash
git clone <repo-url> youtube-skill
cd youtube-skill
claude        # a youtube-figyelem-atalakito skill elérhető
```

### Asztali gépen — B opció (globálisan, minden projektben)
Másold (vagy linkeld) a skill mappáját a személyes skilljeid közé:
```bash
# másolás
cp -r .claude/skills/youtube-figyelem-atalakito ~/.claude/skills/

# VAGY symlink (így a git pull frissíti)
ln -s "$(pwd)/.claude/skills/youtube-figyelem-atalakito" ~/.claude/skills/youtube-figyelem-atalakito
```

## Felépítés

```
.claude/skills/youtube-figyelem-atalakito/
├── SKILL.md                      # a teljes rendszer: alapelv, munkamenet, 45 technika,
│                                 # Attila-féle videóváz, 17 szekciós kimeneti struktúra
├── references/                   # kiegészítő, kompatibilis technika-katalógusok
│   ├── hook-technikak.md
│   ├── nyelvi-fogasok.md
│   ├── figyelemfenntartas.md
│   ├── cim-es-leiras.md
│   ├── vazak.md                  # extra keretrendszerek: PAS / BAB / AIDA, Builder vs Thinker
│   └── peldak.md                 # teljesen kidolgozott példák
└── assets/
    └── forgatokonyv-sablon.md    # kitölthető forgatókönyv-sablon
```

## Frissítés

A technikák bővítéséhez/finomításához szerkeszd a `SKILL.md`-t vagy a
`references/` fájlokat, és commitold. Felhőben a következő session már a
frissített változatot használja; asztali symlink esetén egy `git pull` elég.
