# youtube-skill

Magyar YouTube- és oktatóvideó-ötletek átalakítása nézőközpontú, figyelemmegtartó
tartalommá — **Claude Code skill** formájában.

A skill maga itt található: [`.claude/skills/youtube-figyelem-atalakito/`](.claude/skills/youtube-figyelem-atalakito/)

## Fő elv

> Nem a saját történetemről beszélek. A néző problémájáról beszélek a saját történetemen keresztül.

## Mit csinál?

Egy nyers videóötletből (személyes felismerés, ügyfélhelyzet, oktatási téma) készít:
mélyebb témát, nézőközpontú átírást, 25 címötletet, 8 hookot, Attila-féle 8–11 részes
videóvázat, retenciós tervet, rehookokat, tükörmondatokat, zárásokat és teleprompter-vázlatot
— a teljes, 45 technikából álló rendszer alapján.

## Használat ebben a repóban

Ez egy **projekt-szintű skill**: ha ebben a mappában indítod a Claude Code-ot,
automatikusan elérhető. Hívd meg így:

```text
/youtube-figyelem-atalakito
Van egy videóötletem: ...
```

vagy természetes nyelven:

```text
Használd a youtube-figyelem-atalakito skillt erre az ötletemre: ...
```

## Telepítés máshova (személyes skillként)

Hogy minden projektben elérhető legyen, másold a skill mappáját a személyes skill-könyvtáradba:

```bash
cp -R .claude/skills/youtube-figyelem-atalakito ~/.claude/skills/
```

## Felépítés

```
.claude/skills/youtube-figyelem-atalakito/
├── SKILL.md          # a teljes rendszer (45 technika, kötelező kimeneti struktúra)
├── README.md         # a skill leírása és telepítése
├── examples/         # kész tesztprompt és kitölthető prompt-sablon
└── references/       # nyelvi formulák és technikalisták gyors referenciaként
```
