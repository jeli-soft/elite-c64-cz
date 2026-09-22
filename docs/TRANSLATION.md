# Jak vzniká český překlad Elite pro C64

[Zpět na úvod](../README.md) · [English](TRANSLATION.en.md)

Český překlad Elite pro Commodore 64 zasahuje do textových tabulek, pravidel skládání vět i částí herního kódu. Výsledkem je společné sestavení celé hry, v němž české texty a jejich obsluha tvoří jeden celek.

## Text uložený v tokenech

Paměť C64 je omezená a Elite ji využívá velmi těsně. Text proto ukládá pomocí tokenů: krátkých odkazů na dvojice znaků, slova, části vět nebo další tokeny. Při zobrazení se tyto odkazy rozbalují do výsledného textu. Některé tokeny jsou sdílené napříč hrou a mohou být vnořené do dalších.

Překlad jedné položky tím získává širší dopad. Stejný fragment se může objevit v několika větách nebo obrazovkách. Je třeba kontrolovat všechna jeho použití a podle potřeby upravit i okolní text nebo způsob skládání.

Tokenizace současně určuje, kolik místa text zabere. Delší věta může být při vhodném sdílení úsporná; krátká věta složená převážně z jednotlivých znaků může naopak spotřebovat překvapivě mnoho bajtů. Každá jazyková úprava se tak posuzuje i podle svého vlivu na celé textové tabulky.

## Čeština a skládání vět

Česká slova mění tvar podle pádu, čísla a rodu. Přídavné jméno musí odpovídat podstatnému jménu a správný tvar často závisí na části věty, která vznikne až při jejím sestavování.

Zvlášť náročné jsou procedurálně tvořené popisy planet. Kombinují různé obraty a vlastnosti, které musejí fungovat i ve spojeních, jež při běžném hraní nejsou hned vidět. Úprava jedné varianty může napravit konkrétní popis, ale rozbít jinou kombinaci.

Práce proto zahrnuje volbu vhodných českých formulací, doplnění potřebných tvarů a úpravu pravidel jejich spojování. Součástí kontroly je generování a procházení popisů všech **2 048 systémů v osmi galaxiích**. Tyto kontroly doplňuje ověřování sestavené hry.

## Delší text a pevné hranice paměti

Srozumitelné české formulace často zabírají více místa než původní anglické. Přitom musejí splnit dva odlišné limity: velikost uložených dat a prostor dostupný na obrazovce.

Textové bloky mají v paměti své sousedy a části programu s jejich polohou nebo délkou počítají. Překročení hranice může poškodit jiná data, i když samotný překlad působí správně. Už při dřívější práci se ukázalo, že úspěšné sestavení samo o sobě nezaručuje správné spuštění hry.

Řešení zahrnuje hledání vhodných opakujících se částí, přerozdělení tokenů, úpravy ukazatelů a kontrolu velikostí a adres. Batch111 mimo jiné sjednocuje ukazatele na doplňkové české texty a kontroluje jejich očekávané adresy při sestavení.

## Původní názvy systémů

Některé sdílené tabulky souvisejí také s generováním názvů systémů. Změna dvojic znaků kvůli českému textu by proto mohla změnit i názvy známých planet.

Překlad zachovává původní názvy systémů. Pro jejich generování používá zachované původní dvojice znaků, zatímco české texty mohou využívat upravené tabulky. I tuto změnu bylo nutné začlenit do omezeného paměťového prostoru.

## Text musí fungovat také na obrazovce

Správná věta ještě nemusí dobře vypadat na skutečné herní obrazovce. Kontrolují se šířky řádků, zalamování a umístění textu v tabulkách. Rozhraní má pevný rozměr a delší záhlaví může zasáhnout do sousedního sloupce.

Důležité je i samotné vykreslování. Překrytí textu v některých místech neznamená prosté nahrazení starých písmen novými; může poškodit obraz. Proto je součástí práce kontrola jednotlivých obrazovek, trhu, vybavení, stavových údajů i popisů planet.

## Průběžné zlepšování

**Batch111 je kompletně přeložená a funkční česká verze hry. Na překladu dál pracuji a budu jej vylepšovat.** Další práce se může týkat přirozenějších formulací, vzácných kombinací v popisech i drobných oprav rozhraní.

Při hlášení chyby pomůže konkrétní text, snímek obrazovky a verze hry. U popisu planety je důležitý také název systému a číslo galaxie, aby šlo stejný případ znovu vyvolat.

## Podklady

Technickým základem je rozbor a zdokumentovaný zdrojový kód C64 Elite od Marka Moxona: [Elite source code for the Commodore 64](https://github.com/markmoxon/elite-source-code-commodore-64). Autory původní hry jsou David Braben a Ian Bell; český překlad připravuje **Jeli-softˣ**.
