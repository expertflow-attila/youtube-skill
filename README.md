# youtube-skill

Prémium **Claude Code skill** YouTube videók készítéséhez. Egy nyers ötletből,
oktatóanyagból vagy személyes történetből segít kész **címet, hookot,
forgatókönyvet és videóleírást** formálni — úgy, hogy a néző a te történeteden
keresztül **saját magára ismerjen**, és végignézze a videót.

A skill az alábbi alapelvre épül:

> **Az embereket nem a te történeted érdekli. Az érdekli őket, hogy a
> történetedben felismerik-e saját magukat.**

## Mit tud?

Amikor előhívod és odaadsz neki egy ötletet, végigvezet ezeken:

1. **Az emberi minta** megtalálása — felszíni téma vs. valódi téma (félelem,
   identitás, önbecsapás, bátorság).
2. **Videó típusa** — Builder (tutorial → megoldás) vagy Thinker (probléma →
   felismerés).
3. **6–8 címjavaslat** a tabloid-technikával (konfliktus, tét, kíváncsiság).
4. **2–3 hook-változat** különböző technikákkal (nem mindig kérdéssel!).
5. **Forgatókönyv-váz** az Én→Te→Mi ritmussal, rehookokkal, nyitott hurkokkal.
6. **Videóleírás**, ami nem összefoglal, hanem folytatja a beszélgetést.

A benne lévő összes technika (Tükör-technika, paradoxon, rehook, nyitott hurok,
kontraszt, PAS/BAB/AIDA, mélységi szintek, tabloid címadás stb.) a
`.claude/skills/youtube-storyteller/` mappában van katalogizálva.

## Hogyan hívd elő?

A skill neve: **`youtube-storyteller`**.

- Írd be a Claude Code-ban: `/youtube-storyteller`, majd add meg az ötletet, **vagy**
- egyszerűen mondd el az ötleted, és kérd, hogy a YouTube-skilllel dolgozzon rajta
  (a Claude a leírás alapján magától is előhívja).

Példák:
- „Van egy ötletem egy videóhoz arról, hogy elvesztem az AI-ban — segíts a
  youtube-storyteller skillel."
- „Csinálj címet és hookot ehhez az oktatóvideóhoz: n8n automatizáció kezdőknek."

## Telepítés / elérés

### Felhőben (Claude Code on the web)
Semmi teendő. A skill ebben a repóban él (`.claude/skills/`), így amikor ezen a
repón indítasz felhős sessiont, **automatikusan elérhető**. Csak hívd elő.

### Asztali gépen — A opció (ezen a repón belül)
Klónozd a repót, és dolgozz benne — a project-skill automatikusan betöltődik:
```bash
git clone <repo-url> youtube-skill
cd youtube-skill
claude        # a youtube-storyteller skill elérhető
```

### Asztali gépen — B opció (globálisan, minden projektben)
Másold (vagy linkeld) a skill mappáját a személyes skilljeid közé, így bármelyik
projektben előhívható:
```bash
# másolás
cp -r .claude/skills/youtube-storyteller ~/.claude/skills/

# VAGY symlink (így a git pull frissíti)
ln -s "$(pwd)/.claude/skills/youtube-storyteller" ~/.claude/skills/youtube-storyteller
```

## Felépítés

```
.claude/skills/youtube-storyteller/
├── SKILL.md                      # vezérlő: alapelv, munkafolyamat, checklist
├── references/
│   ├── hook-technikak.md         # 9 nyitási technika
│   ├── nyelvi-fogasok.md         # „mit mondjak helyette" — Rossz→Jobb átírások
│   ├── figyelemfenntartas.md     # Én→Te→Mi ritmus, rehook, nyitott hurok, kontraszt
│   ├── cim-es-leiras.md          # tabloid címadás + videóleírás-minta
│   ├── vazak.md                  # PAS/BAB/AIDA, univerzális váz, Builder vs Thinker
│   └── peldak.md                 # teljesen kidolgozott példák
└── assets/
    └── forgatokonyv-sablon.md    # kitölthető forgatókönyv-sablon
```

## Frissítés

A technikák bővítéséhez szerkeszd a `references/` fájlokat, és commitold.
Felhőben a következő session már a frissített változatot használja; asztali
symlink esetén egy `git pull` elég.
