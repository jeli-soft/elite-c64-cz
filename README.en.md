# Elite for the Commodore 64 — Czech translation

[Česky](README.md)

A complete, playable **Czech translation of Elite for the Commodore 64** by **Jeli-softˣ**. The current version is **batch111**, based on the **GMA86 PAL** variant.

**I am continuing to work on and improve the translation.** Batch111 is the current playable version; future releases may refine the wording, fix issues and improve the text.

## Download and run

**[Download the Czech game — batch111 (.d64)](https://github.com/jeli-soft/elite-c64-cz/raw/refs/heads/main/downloads/elite-c64-cz-batch111-pal.d64)**

The disk image contains the complete translated game. It is intended for a PAL Commodore 64 with a 1541 drive, or an emulator configured accordingly, such as [VICE](https://vice-emu.sourceforge.io/).

1. Attach the D64 image to an emulated 1541 drive, or use compatible disk-image equipment with a real C64.
2. Start the game from the attached disk.
3. If the loader asks whether to use fast loading, choose **N** to use standard loading.

The in-game text is Czech **without diacritics**. The download's checksum is available in [SHA256SUMS.txt](downloads/SHA256SUMS.txt).

## What the translation involves

The Czech text is integrated into the game's code and data. Elite uses shared and nested text tokens, and constructs some sentences at runtime. A single change can therefore affect several different parts of the game.

Czech introduces requirements for inflection, gender, number and grammatical agreement. Clear Czech wording also often needs more space. The work includes revising tokenization and sentence construction, checking system names, memory limits and line lengths, and verifying the result in the game.

Read [How the Czech translation works](docs/TRANSLATION.en.md) for more detail. Release notes are in [CHANGELOG.md](CHANGELOG.md).

## Translation feedback

Please use [Issues](https://github.com/jeli-soft/elite-c64-cz/issues) to report a problem or suggest better wording. Include the game version, the relevant screen or system, and a screenshot of the text where possible. For a planet-description issue, include the galaxy number as well.

## Screenshots

### Title screen and commander loading

![Title screen and commander loading](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230301.png)

### Czech start prompt

![Czech start prompt](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230437.png)

### Commander Jameson's status and ship equipment

![Commander Jameson's status and ship equipment](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230527.png)

### Ship equipment shop

![Ship equipment shop](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230614.png)

### Commodity prices in the Lave market

![Commodity prices in the Lave market](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230738.png)

### Lave's data and Czech planet description

![Lave's data and Czech planet description](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20230828.png)

### Eninre's data and Czech planet description

![Eninre's data and Czech planet description](img/Sn%C3%ADmek%20obrazovky%202026-09-22%20231156.png)

## Credits and sources

- Original **Elite**: **David Braben and Ian Bell**.
- Czech translation: **Jeli-softˣ**.
- Analysis and documented C64 source code: **Mark Moxon**, [Elite source code for the Commodore 64](https://github.com/markmoxon/elite-source-code-commodore-64).

Rights to the original game remain with their respective holders. This project does not grant a new licence to the original game.
