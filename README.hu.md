# ForgeWin for Mac

![ForgeWin ikon](assets/forgewin.png)

Windows 10 és Windows 11 telepítőpendrive készítése Macen, natív magyar és angol felülettel.

**Bétaverzió. A készítés a kiválasztott USB-meghajtó minden partícióját és adatát törli.** A szükséges adataidról előtte készíts mentést.

[Letöltés a Releases oldalról](https://github.com/macrobi/ForgeWin/releases) · [English](README.md)

## Képernyőképek

A képekre kattintva teljes méretben nézheted meg őket.

| | |
| --- | --- |
| **Windows ISO letöltése**<br>[![Windows ISO letöltése](assets/screenshots/ForgeWin01.png)](assets/screenshots/ForgeWin01.png) | **USB-meghajtó kiválasztása**<br>[![USB-meghajtó kiválasztása](assets/screenshots/ForgeWin02.png)](assets/screenshots/ForgeWin02.png) |
| **A meghajtó törlésének megerősítése**<br>[![A meghajtó törlésének megerősítése](assets/screenshots/ForgeWin03.png)](assets/screenshots/ForgeWin03.png) | **Nagy Windows-kép darabolása**<br>[![Nagy Windows-kép darabolása](assets/screenshots/ForgeWin04.png)](assets/screenshots/ForgeWin04.png) |
| **A telepítő másolása**<br>[![A telepítő másolása](assets/screenshots/ForgeWin05.png)](assets/screenshots/ForgeWin05.png) | **A másolt fájlok ellenőrzése**<br>[![A másolt fájlok ellenőrzése](assets/screenshots/ForgeWin06.png)](assets/screenshots/ForgeWin06.png) |
| **Műveleti előzmények**<br>[![Műveleti előzmények](assets/screenshots/ForgeWin07.png)](assets/screenshots/ForgeWin07.png) |  |

## Követelmények

- macOS 14 vagy újabb. Az alkalmazás Apple Silicon és Intel változatot is tartalmaz.
- Külön beszerzett, hivatalos Windows 10 vagy Windows 11 **x64** ISO.
- Külső fizikai USB-meghajtó, legfeljebb 2 TB kapacitással és elegendő hellyel.
- Nagy Windows-kép darabolásakor szabad ideiglenes tárhely a Macen.

A telepítő **x64 UEFI PC-hez** készül. Legacy BIOS és ARM Windows nem támogatott. A ForgeWin nem telepít Windowst az őt futtató Macre.

## Telepítés és használat

1. A [Releases oldalon](https://github.com/macrobi/ForgeWin/releases) válaszd a béta kiadást, és töltsd le a `.dmg` fájlt. Az automatikus „Source code” archívumok csak a repó dokumentációját tartalmazzák.
2. Nyisd meg a lemezképet, húzd a **ForgeWin** alkalmazást az **Alkalmazások** mappába, és onnan indítsd el.
3. Válaszd ki a Windows ISO-t és a pendrive-ot. Ellenőrizd a célmeghajtó adatait.
4. Erősítsd meg a célt, és indítsd el a készítést. Várd meg a biztonságos eltávolítást jelző üzenetet.

Az alapértelmezés GPT és FAT32; MBR is választható UEFI használathoz. A program automatikusan darabolja a nagy `install.wim` fájlt, másol, majd SHA-256 összehasonlítást végez visszaolvasással. A sikeres ellenőrzés nem bizonyítja a PC-s indíthatóságot.

A szükséges WIM-eszköz az alkalmazás része. Homebrew és felhasználói fiók nem kell. Részletes magyar útmutatót a helyi Súgó menüben találsz.

## A béta állapota

**0.3 beta, build 6.** Ennél a kiadásnál még ellenőrizendő a valódi PC-s UEFI/Secure Boot indítás és Windows-telepítés, valamint a fizikai Intel Macen és macOS 14-en történő futás. Az [angol kiadási jegyzet](docs/RELEASE_NOTES.md) összefoglalja a korlátokat.

Hibát az [Issues oldalon](https://github.com/macrobi/ForgeWin/issues) jelezhetsz magyarul is. Írd meg az app és a macOS verzióját, a Mac és a pendrive típusát, valamint a hiba pontos szövegét. A naplókból és képekből töröld a személyes útvonalakat és fájlneveket.

## Adatkezelés és szerzői jog

Az ISO és az USB feldolgozása helyben történik. Nincs analitika, követés vagy automatikus naplóküldés. Az utolsó művelet előzménye és az utolsó hiba a Macen marad. A Microsoft letöltési hivatkozásai a böngészőben nyílnak meg.

Copyright Veress Róbert 2026. A ForgeWin saját forráskódja privát; ez a repó a terjesztési dokumentációt tartalmazza. A csomagolt wimlib külön licencű komponens; licencei, eredeti forrása és újraépítési scriptje az alkalmazásban megtalálható. [Részletek](THIRD_PARTY_NOTICES.md).

A ForgeWin nem Microsoft-termék. Windows ISO-t és Windows-licencet nem tartalmaz.
