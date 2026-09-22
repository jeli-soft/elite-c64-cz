# Elite pro Commodore 64 — český překlad

[English](README.en.md)

Kompletně přeložená, funkční česká verze hry **Elite pro Commodore 64** od **Jeli-softˣ**. Aktuálně je k dispozici **batch111**, vycházející z varianty **GMA86 pro PAL**.

**Na překladu dál pracuji a budu jej průběžně vylepšovat.** Batch111 je současná hratelná verze; další vydání mohou přinést jazykové úpravy, opravy a zpřesnění textů.

## Stažení a spuštění

**[Stáhnout českou hru — batch111 (.d64)](https://github.com/jeli-soft/elite-c64-cz/raw/refs/heads/main/downloads/elite-c64-cz-batch111-pal.d64)**

Obraz diskety obsahuje celou přeloženou hru. Je určený pro Commodore 64 v režimu PAL s mechanikou 1541 nebo pro odpovídající nastavení emulátoru, například [VICE](https://vice-emu.sourceforge.io/).

Texty ve hře jsou česky **bez diakritiky**. Kontrolní součet staženého souboru najdete v [SHA256SUMS.txt](downloads/SHA256SUMS.txt).

## Co překlad obnáší

České texty jsou začleněné do herního kódu a dat. Elite používá sdílené a vnořené textové tokeny a část vět skládá za běhu. Jediná úprava tak může ovlivnit několik různých míst ve hře.

Čeština přidává nároky na skloňování, rod, číslo a shodu. Srozumitelná česká formulace také často potřebuje více místa. Práce proto zahrnuje přepracování tokenizace a skládání vět, kontrolu názvů systémů, paměťových limitů a délky řádků i ověřování výsledku ve hře.

Podrobnosti popisuje [Jak vzniká český překlad](docs/TRANSLATION.md). Přehled vydání je v [CHANGELOG.md](CHANGELOG.md).

## Připomínky k překladu

Chyby nebo vlastní návrhy můžete popsat v [Issues](https://github.com/jeli-soft/elite-c64-cz/issues).

## Ukázky ze hry

### Úvodní obrazovka s načtením velitele

![Úvodní obrazovka s načtením velitele](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230301.png)

### Česká výzva ke spuštění hry

![Česká výzva ke spuštění hry](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230437.png)

### Stav velitele Jamesona a vybavení lodi

![Stav velitele Jamesona a vybavení lodi](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230527.png)

### Nákup vybavení lodi

![Nákup vybavení lodi](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230614.png)

### Ceny zboží na trhu systému Lave

![Ceny zboží na trhu systému Lave](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230738.png)

### Údaje a český popis planety Lave

![Údaje a český popis planety Lave](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230828.png)

### Údaje a český popis planety Eninre

![Údaje a český popis planety Eninre](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20231156.png)

## Autoři a podklady

- Původní **Elite**: **David Braben a Ian Bell**.
- Český překlad: **Jeli-softˣ**.
- Rozbor a zdokumentované zdrojové kódy verze pro C64: **Mark Moxon**, [Elite source code for the Commodore 64](https://github.com/markmoxon/elite-source-code-commodore-64).

Práva k původní hře náleží jejím příslušným držitelům. Tento projekt k ní neuděluje novou licenci.
