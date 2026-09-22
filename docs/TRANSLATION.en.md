# How the Czech translation of C64 Elite works

[Back to the project](../README.en.md) · [Česky](TRANSLATION.md)

Translating Elite for the Commodore 64 into Czech involves text tables, sentence-generation rules and parts of the game code. The result is a complete game build in which the Czech text and the routines handling it are integrated.

## Text stored as tokens

The C64 has limited memory, and Elite uses it tightly. Text is stored using tokens: compact references to character pairs, words, sentence fragments or other tokens. These references are expanded when the text is displayed. Some tokens are shared across the game and can be nested inside others.

Changing one entry therefore has wider consequences. The same fragment may appear in several sentences or screens. Every use needs checking, and sometimes the surrounding text or the way the sentence is assembled needs changing too.

Tokenization also determines how much storage the text needs. A longer sentence can be economical when it reuses suitable fragments, while a short sentence stored mostly as individual characters can consume a surprising number of bytes. Each wording change must therefore be considered in the context of the complete text tables.

## Czech grammar and generated sentences

Czech words change form according to case, number and gender. Adjectives must agree with nouns, and the correct form often depends on a part of the sentence chosen during generation.

Procedurally generated planet descriptions are particularly demanding. Their phrases and properties must work in combinations that may not appear during a short play session. Adjusting one variant can improve a particular description while breaking another combination.

The work includes finding suitable Czech wording, supplying the necessary inflected forms and adapting the rules that combine them. Validation includes generating and reviewing descriptions for all **2,048 systems across eight galaxies**, alongside checks in the built game.

## Longer text and fixed memory boundaries

Clear Czech wording often takes more space than the original English. It must meet two separate constraints: the size of the stored data and the space available on screen.

Text blocks share memory with other data, and parts of the program depend on their location or size. Crossing a boundary can damage neighbouring data even when the translation itself looks correct. Earlier work demonstrated that successful assembly alone does not guarantee that the game will start correctly.

The solutions include finding reusable fragments, reorganizing tokens, adjusting pointers and checking sizes and addresses. Among other changes, batch111 consolidates pointers to additional Czech text and checks their expected addresses during assembly.

## Preserving system names

Some shared tables also contribute to system-name generation. Changing character pairs to suit Czech text could therefore alter familiar planet names.

The translation preserves the original system names. Their generation uses the original character pairs, while Czech text can use revised tables. This separation also had to fit within the available memory.

## Text must work on screen

A grammatically correct sentence still needs to fit the actual game screen. Line width, wrapping and table alignment all need checking. The interface has fixed dimensions, and a longer heading can overlap the next column.

Rendering matters as well. In some places, drawing text over existing text does not simply replace the old letters; it can corrupt the display. Checks therefore cover the individual screens, market, equipment, status information and planet descriptions.

## Continued improvement

**Batch111 is a complete, playable Czech translation of the game. I am continuing to work on and improve it.** Further changes may refine the wording, address rare description combinations or fix small interface issues.

A useful report includes the exact text, a screenshot and the game version. For a planet description, include the system name and galaxy number so the same case can be reproduced.

## Sources

The technical foundation is Mark Moxon's analysis and documented C64 Elite source code: [Elite source code for the Commodore 64](https://github.com/markmoxon/elite-source-code-commodore-64). The original game was created by David Braben and Ian Bell; the Czech translation is by **Jeli-softˣ**.
