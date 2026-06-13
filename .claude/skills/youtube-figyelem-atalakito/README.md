# youtube-figyelem-atalakito

Claude Code skill magyar YouTube- és oktatóvideó-ötletek átalakítására.

## Mit csinál?

Nyers videóötletből készít:

- valódi, mélyebb témát
- nézőközpontú átfordítást
- kötelező átírási táblázatot
- YouTube címötleteket
- hookokat / nyitásokat
- Attila-féle 8–11 részes videóvázat
- retenciós tervet
- rehookokat
- visszadobó és visszahúzó mondatokat
- tükörmondatokat
- oktatói tanulságokat
- zárásokat
- teleprompter-vázlatot
- technikatérképet

## Fő elv

> Nem a saját történetemről beszélek. A néző problémájáról beszélek a saját történetemen keresztül.

## V3 lényege

A V3 már nem csak a Tükör-technikára épül. A teljes rendszer belekerült, különösen ezek:

1. Tükör-technika
2. Tükörnyitás
3. Kimondatlan érzés megnevezése
4. „Talán te is...” technika
5. Visszadobás
6. Rejtett minta
7. Nyitott hurkok / open loop
8. Kontraszt
9. Kérdés, ami nem kér választ
10. „Én” helyett „Te”
11. „Én” helyett „Mi”
12. Esemény → emberi minta
13. Állítás → kérdés
14. Konkrétum → érzés
15. Tanítás → felfedezés
16. Történet → tükör
17. „Talán” formula
18. „Lehet, hogy” formula
19. „Ismerős?” technika
20. Visszahúzó mondatok
21. Én → Te → Mi pingpong
22. Rejtett probléma technika
23. „Valójában nem erről szól” technika
24. Központi kérdés technika
25. Paradoxon technika
26. „Én csak a bizonyíték vagyok” technika
27. „Te is” technika
28. Néző a hős technika
29. Közös ellenség technika
30. Néző belső mondata technika
31. Tabloid címtechnika
32. Veszteség / tét technika
33. Kellemetlen igazság technika
34. Kérdés-hook technika
35. „Azt hittem X, de valójában Y” hook
36. Feszültség → feloldás → új feszültség
37. Rehook technika
38. Pattern interrupt technika
39. Konkrétból univerzális technika
40. Példa-létra technika
41. Oktatás történeten keresztül technika
42. Mélyebb igazság technika
43. Csend ára technika
44. Visszafordító zárás technika
45. Anti-bullshit stílustechnika

## Telepítés Claude Code-ba

Személyes skillként:

```bash
mkdir -p ~/.claude/skills
cp -R youtube-figyelem-atalakito ~/.claude/skills/
```

Projekt skillként:

```bash
mkdir -p .claude/skills
cp -R youtube-figyelem-atalakito .claude/skills/
```

Ezután Claude Code-ban használhatod például így:

```text
/youtube-figyelem-atalakito
Van egy videóötletem: ...
```

Vagy természetes nyelven:

```text
Használd a youtube-figyelem-atalakito skillt erre az ötletemre: ...
```

## Tesztprompt

Lásd: `examples/teszt-prompt.md`
