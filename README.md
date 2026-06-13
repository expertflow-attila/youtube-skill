# YouTube Figyelem Átalakító 🎬

Ez a repó egy **rendszer a YouTube-videóid elkészítéséhez**. A lényege egy Claude
Code **Skill**, amely a nyers videóötleteidet — személyes felismeréseket,
ügyfélhelyzeteket, oktatási témákat — nézőközpontú, figyelemmegtartó videótervvé
alakítja magyar nyelven.

A vezérelv:

> Nem a saját történetemről beszélek. A néző problémájáról beszélek a saját
> történetemen keresztül.

---

## Mit csinál?

Amikor azt mondod Claude-nak, hogy *„van egy YouTube-ötletem"*, a skill
automatikusan végigvisz egy teljes rendszeren, és a végén egy **17 pontos
videótervet** kapsz:

1. Rövid diagnózis (felszíni téma, valódi konfliktus, kimondatlan érzés…)
2. A videó valódi témája
3. Kötelező átírási táblázat (rólam szóló → nézőközpontú)
4. 5 központi kérdés
5. 25 címötlet (5 kategóriában)
6. A legjobb 1–3 cím elemzése
7. 8 különböző hook / nyitás
8. Attila-féle videóváz 8–11 résszel
9. Retenciós terv (másodpercre bontva)
10. 20+ rehook és visszadobás mondat
11. 15 tükörmondat
12. 12 nyelvi formula
13. Oktatói tanulságok
14. 5 zárás
15. Rövid teleprompter vázlat
16. Technikák térképe
17. Ajánlott végső csomag

Nem csak a **Tükör-technikát** használja, hanem egy **45 elemből álló teljes
technikatárat**: címtechnika, tükörnyitás, kimondatlan érzés, kontraszt,
paradoxon, open loop, rehook, mélyebb igazság, visszafordító zárás és így tovább.

---

## Hogyan használd?

### A Claude Code weben / appban (ez a repó)

Mivel a skill a repó `.claude/skills/` mappájában van, **automatikusan elérhető**,
amikor ebben a repóban dolgozol. Csak írd le az ötletedet, például:

> Van egy videóötletem: három évig csak AI-eszközöket hajkurásztam, és közben
> elvesztettem a fókuszt. Csináljunk ebből videót, de ne csak rólam szóljon.

Vagy hívd meg közvetlenül:

> /youtube-figyelem-atalakito Van egy ötletem egy halogatott ügyfélbeszélgetésről…

A skill filléres bemenetből is dolgozik — ha hiányzik valami, ésszerű
feltételezést tesz, és jelzi: *„Feltételezésem: …"*.

### Ha mindenhol szeretnéd használni (nem csak ebben a repóban)

Másold a skill mappáját a globális skillek közé:

```bash
cp -r .claude/skills/youtube-figyelem-atalakito ~/.claude/skills/
```

Ezután bármelyik projektben elérhető lesz.

---

## A repó felépítése

```
.
├── README.md                  ← ez a fájl
├── CLAUDE.md                  ← projekt-szintű utasítás (a skill mindig aktiválódik)
└── .claude/
    └── skills/
        └── youtube-figyelem-atalakito/
            ├── SKILL.md       ← a rendszer szíve: munkamenet + 17 pontos kimenet
            └── references/
                ├── technikatar.md   ← a teljes, 45 elemű technikatár példákkal
                ├── videovaz.md      ← az Attila-féle videóváz (11 lépés)
                └── pelda.md         ← példa bemenet és kimeneti irány
```

---

## Mire jó a bemenet? (nem kötelező, de segít)

A skill töredékes, beszélt nyelvű inputból is dolgozik. Ha van rá módod, ezek
segítenek: nyers videóötlet · munkacím · miről akarsz beszélni · saját
történet/felismerés · célközönség · milyen érzést akarsz kiváltani · oktató /
vallomásos / provokatív / hibrid · platform (longform, Shorts, TikTok, LinkedIn).

---

## Stílus

**Legyen:** magyar, közvetlen, emberi, őszinte, mély de érthető, vállalkozói de
nem marketinges, személyes de nézőközpontú, gondolkodtató de nem okoskodó.

**Kerüld:** AI-szagú általánosságokat, guru-hangnemet, üres nagy szavakat,
„Ebben a videóban arról lesz szó…" kezdést, túl sok „én" fókuszt.

---

## Megjegyzés a feltöltött anyagról

Ez a rendszer a `youtube-figyelem-atalakito` skill **3.0.0** verziójára épül. Ha
van további nyersanyagod (pl. a „youtube-figyelem-atalakito 2" mappa fájljai,
korábbi videószkriptek, jó és rossz példák, saját nyelvi fordulatok), azokat is
hozzá lehet adni a `references/` mappához vagy egy új `knowledge/` mappához
tudásként — minél több valódi példa van, annál pontosabban illeszkedik a skill a
te hangodhoz.
