---
title: Rašmenų koduotės
type: page
aliases:
    - /standartai/rašmenų-koduočių-standartai/
menu:
    main:
        weight: 20
        parent: Standartai
---

LST ISO/IEC 10646-1 (UCS, Unikodas)
-----------------------------------

**_Lietuvos standartas LST ISO/IEC 10646-1. Universalus keliais baitais koduotų ženklų rinkinys. 1 dalis. Sandara ir pagrindinė daugiakalbė lentelė._**

ISO/IEC 10646 (angl. _Universal Coded Character Set_, UCS) ir Unikodas yra du stipriai tarpusavyje suderinti standartai, kuriami dviejų atskirų glaudžiai bendradarbiaujančių organizacijų.
Pirmąjį sukūrė ir tobulina [Tarptautinė standartų organizacija (ISO)][Tarptautinė standartų organizacija], o antrąjį – [„Unicode“ konsorciumas][„Unicode“ konsorciumas].

Nors standartas ISO/IEC 10646 apibrėžia ženklų kodavimą 32 bitais (4 baitais), o Unikodas – 16 bitų (2 baitais), šiuo metu abu standartai numato galimybę užkoduoti kiek virš 1,1 milijono skirtingų ženklų.
Faktinė užkoduotų ženklų aibė yra žymiai mažesnė, tačiau ji nuolatos didėja, nes [kasmet išleidžiamos][Unikodo versijos] naujos Unikodo versijos.

Pastebėtina, kad Unikodas nėra koduotė – tai rašto ženklų rinkinys, kuriame kiekvienas ženklas turi konkrečią priskirtą poziciją (numerį, angliškai vadinamą _code point_).
Kalbant apie konkrečias Unikodo pozicijas, jos paprastai žymimos užrašu „U+xxxx“, kur „xxxx“ – pozicijos numeris šešioliktainiu formatu, pavyzdžiui, raidė „O“ užrašoma taip: U+004F.
Unikodo standarte aprašyti trys šių ženklų kodavimo (vertimo konkrečiomis baitų sekomis) būdai, arba koduotės: UTF-8, UTF-16 ir UTF-32. Praktikoje yra naudojami dar keli.

Unikodo pozicijų numeriai dažnai vadinami Unikodo kodais, tačiau būtina suprasti, jog U+xxxx reiškia **ne konkrečią baitų seką, bet pozicijos numerį**.
Konkreti baitų seka visuomet priklauso nuo naudojamos koduotės.

Unikodą galima laikyti ISO standarto viršaibiu, nes jis aprašo ne tik ženklų kodavimą, bet ir rikiavimo, išraiškų normalizavimo, teksto krypties taisykles ir kai kuriuos kitus dalykus apie kuriuos ISO standarte nekalbama.
Tinkamam daugiakalbystės palaikymui vien tik ISO standartą palaikyti nepakanka – būtina tinkamai realizuoti ir Unikodo palaikymą.
Neformalioje kalboje skirtumas tarp šių standartų dažniausiai neakcentuojamas ir kalbama tiesiog apie Unikodą.

Unikode yra visos pagrindinės ir 33 kirčiuotos lietuviškos abėcėlės raidės.
Likusias 35 kirčiuotas raides galima išreikšti kompozicinėmis sekomis.
Kompozicinę seką sudaro paeiliui einantys pamatinės raidės ir kombinacinio kirčio kodai, o mažųjų raidžių **i**, **į**, ir **j** atvejais tarp jų įsiterpia ir kombinacinio taško kodas.
Pavyzdžiui, raidė **m̃** (mažoji raidė m su riestiniu kirčiu) išreiškiama kodų seka U+006D U+0303, o raidė **į̇́** (mažoji raidė i nosinė su dešininiu kirčiu) – kodų seka U+012F U+0307 U+0301.

Kone visuose kituose koduočių standartuose, bent jau patvirtintuose ar atnaujintuose nuo 2000 metų, ISO/IEC 10646 standartas naudojamas kaip atspirties taškas – konkrečios pozicijos tose koduotėse yra vienareikšmiškai įvardijamos kaip konkrečių jo pozicijų ar sekų atitikmenys.

Lietuvoje standartas ISO/IEC 10646-1 yra priimtas viršelio būdu ir jam suteiktas žymuo LST ISO/IEC 10646-1.

8 bitų koduotės
---------------

Prieš išrandant Unikodą ir jam įsigalint, kompiuteriuose buvo vartojama daugybė tarpusavyje nesuderinamų ženklų koduočių.
Daugumoje šių koduočių ženklai buvo koduojami vienu baitu, todėl į tokias koduotes tilpdavo tik nedidelė aibė ženklų
Žemiau rasite dalies lietuvių kalbai naudotų (ar standartizuotų naudoti) 8 bitų koduočių sąrašą.
Aštuonbičių koduočių, ypač Lietuvos kompiuterizavimo pradžioje, buvo dar daugiau.
Apie kai kurias jų šiais laikais praktiškai nelikę jokios informacijos.

Atkreipkite dėmesį, jog šiandien visos šios koduotės aktualios tik atvirkštinio suderinamumo tikslais – kai reikia galimybės dirbti su jomis užkoduotais duomenimis.
Visose naujose programose ir sistemose kaip pagrindinę koduotę derėtų naudoti tik Unikodą.

Daugumos aštuonbičių koduočių žemesnioji pusė (pirmos 128 pozicijos) sutampa su 7 bitų ASCII koduote. Su ja taip pat sutampa ir pirmos 128 Unikodo pozicijos. Jos atrodo štai taip ir žemiau nebus kartojamos:

<div style="font-size:150%">

|    | …0 | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D | …E | …F |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0… | ␀  | ␁  | ␂  | ␃  | ␄  | ␅  | ␆  | ␇  | ␈  | ␉  | ␊  | ␋  | ␌  | ␍  | ␎  | ␏  |
| 1… | ␐  | ␑  | ␒  | ␓  | ␔  | ␕  | ␖  | ␗  | ␘  | ␙  | ␚  | ␛  | ␜  | ␝  | ␞  | ␟  |
| 2… | ␠  | \! | "  | #  | $  | %  | &  | '  | (  | )  | \* | +  | ,  | \- | .  | /  |
| 3… | 0  | 1  | 2  | 3  | 4  | 5  | 6  | 7  | 8  | 9  | :  | ;  | <  | \= | \> | ?  |
| 4… | @  | A  | B  | C  | D  | E  | F  | G  | H  | I  | J  | K  | L  | M  | N  | O  |
| 5… | P  | Q  | R  | S  | T  | U  | V  | W  | X  | Y  | Z  | \[ | \\ | \] | ^  | \_ |
| 6… | \` | a  | b  | c  | d  | e  | f  | g  | h  | i  | j  | k  | l  | m  | n  | o  |
| 7… | p  | q  | r  | s  | t  | u  | v  | w  | x  | y  | z  | {  | \| | }  | ~  | ␡  |

</div>

Šioje ir kitose lentelėse koduotės ženklai išvardinti kone įprasčiausiu koduotėms būdu – eilučių ir stulpelių antraštėse naudojant šešioliktainius skaitmenis, o eilutės ir stulpelio sandūroje – nurodant konkrečioje šešioliktainėje pozicijoje esantį ženklą.
Pavyzdžiui, eilutės „5…“ ir stulpelio „…9“ sandūroje nurodyta raidė Y, esanti visų čia minimų koduočių 59-ojoje šešioliktainėje (131-ojoje dešimtainėje) pozicijoje.
Pozicijos numeruojamos nuo nulio – tuomet pats pozicijos numeris atspindi aštuonbitės koduotės kodą.
Pozicijos nuo 00 iki 1F imtinai bei 7F yra naudojamos vadinamiesiems nespausdinamiems, arba kontroliniams ženklams. Lentelėje šie ženklai pakeisti jų grafiniam atvaizdavimui skirtais Unikodo ženklais.
20 pozicijoje yra paprastas tarpas – jis irgi pakeistas grafiniam atvaizdavimui skirtu ženklu.

Žemiau esančiose kai kurių koduočių viršutinių dalių (128-255) lentelėse pirmos dvi eilutės (pozicijos 80-9F) yra tuščios.
Taip yra dėl to, kad tose koduotėse šios pozicijos (kaip ir 00–1F bei 7F) yra rezervuotos nespausdinamiems ženklams, tačiau patys ženklai neįvardyti.
Praktikoje galima laikyti, jog šie kodai atitinka tas pačias pozicijas Unikodo ženklų aibėje.
Lentelėse naudojami šie žymėjimai: NBSP – jungiamasis tarpas (angl. _non-breaking space_); SHY – kėlimo ženklas (angl. _soft hyphen_).

### LST ISO/IEC 8859-13

**_Lietuvos standartas LST ISO/IEC 8859-13. Informacijos technologija. 8 bitais koduotų ženklų rinkiniai. 13 dalis.
Lotynų 7-oji abėcėlė (tapatus ISO/IEC 8859-13:1998)._**

Tarptautiniu mastu rašto ženklų kodavimą 8 bitais apibrėžia standartas [ISO/IEC 8859][ISO 8859].
Jį sudaro atskiros dalys, kurių kiekviena dalis apibrėžia kodų lentelę, pritaikytą tam tikros kalbų grupės rašto ženklams koduoti.
Standartas yra atviras, t. y. gali būti papildomas naujomis dalimis. Šiuo metu jį sudaro 15 dalių.

Standarto 13-oji dalis ISO/IEC 8859-13 apibrėžia lotynų 7-osios abėcėlės ženklų rinkinį, turintį lietuviškus rašto ženklus.
Ji išversta į lietuvių kalbą ir priimta Lietuvos standartu, kuriam suteiktas žymuo [LST ISO/IEC 8859-13:2000][ISO 8859-13 vaizdas].
Šio standarto apibrėžta kodų lentelė kompiuteriuose žymima trumpiau – ISO-8859-13.
Tai – pagrindinis Lietuvos rašto ženklų kodavimo 8 bitais standartas, naudotas kaip pagrindas kuriant kitus 8 bitų kodavimo standartus.

Standartas LST ISO/IEC 8859-13 nuo 2000 m. pakeitė iki tol galiojusį standartą LST 1282. Tačiau iš tikrųjų pasikeitė tik
aprašymo pavidalas, o visų ženklų kodai išliko tie patys.
LST 1282 standarto koduotė dar buvo žinoma „Baltic Rim“ vardu.
Ją projektavo Virginijus Dadurkevičius, Evaldas Kulbokas, Imants Mētra, Edmundas Mišeikis, Algimantas Oškinis, Danielius Ralys.

Apatinė šios koduotės pusė (128-255 pozicijos) atrodo taip:

<div style="font-size:150%">

|    | …0   | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D  | …E | …F |
|----|------|----|----|----|----|----|----|----|----|----|----|----|----|-----|----|----|
| 8… |      |    |    |    |    |    |    |    |    |    |    |    |    |     |    |    |
| 9… |      |    |    |    |    |    |    |    |    |    |    |    |    |     |    |    |
| A… | NBSP | ”  | ¢  | £  | ¤  | „  | ¦  | §  | Ø  | ©  | Ŗ  | «  | ¬  | SHY | ®  | Æ  |
| B… | °    | ±  | ²  | ³  | “  | µ  | ¶  | ·  | ø  | ¹  | ŗ  | »  | ¼  | ½   | ¾  | æ  |
| C… | Ą    | Į  | Ā  | Ć  | Ä  | Å  | Ę  | Ē  | Č  | É  | Ź  | Ė  | Ģ  | Ķ   | Ī  | Ļ  |
| D… | Š    | Ń  | Ņ  | Ó  | Ō  | Õ  | Ö  | ×  | Ų  | Ł  | Ś  | Ū  | Ü  | Ż   | Ž  | ß  |
| E… | ą    | į  | ā  | ć  | ä  | å  | ę  | ē  | č  | é  | ź  | ė  | ģ  | ķ   | ī  | ļ  |
| F… | š    | ń  | ņ  | ó  | ō  | õ  | ö  | ÷  | ų  | ł  | ś  | ū  | ü  | ż   | ž  | ’  |
</div>

### LST 1564

**_Lietuvos standartas LST 1564. Informacijos technologija. Ženklų kodavimas 8 bitais. Lietuviškų kirčiuotų raidžių
rinkinys_**

Kirčiuotų raidžių standartas apibrėžia [kodų lentelę][LST 1564 vaizdas], kurioje pagrindinės lietuvių kalbos abėcėlės raidžių aibė papildyta kirčiuotomis raidėmis.
Šioje kodų lentelėje pagrindinių (nekirčiuotų) lietuviškos abėcėlės raidžių ir visų kitų ženklų, išskyrus kirčiuotas raides, kodai sutampa su standarto LST ISO/IEC 8859-13 kodais.

Šis standartas buvo pagrindinis 8 bitais koduojamų kirčiuotų raidžių standartas.
Remiantis šiuo standartu buvo sudaromi kirčiuotų raidžių kodavimo standartai atskiroms operacinėms sistemoms.

Aukštesnioji šios koduotės pusė (128-255 pozicijos) atrodo taip:

<div style="font-size:150%">

|    | …0   | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D  | …E | …F |
|----|------|----|----|----|----|----|----|----|----|----|----|----|----|-----|----|----|
| 8… |      |    |    |    |    |    |    |    |    |    |    |    |    |     |    |    |
| 9… |      |    |    |    |    |    |    |    |    |    |    |    |    |     |    |    |
| A… | NBSP | Ą̃  | Ę́  | Ę̃  | i̇̃  | L̃  | M̃  | m̃  | Ė́  | Ñ  | Ė̃  | R̃  | Ų́  | SHY | Ū̃  | Ū́  |
| B… | Ĩ    | ą̃  | ę́  | ę̃  | ´  | l̃  | ¶  | j̇̃  | ė́  | ñ  | ė̃  | r̃  | ų́  | Ų̃   | ū̃  | ū́  |
| C… | Ą    | Į  | À  | Á  | Ä  | Ã  | Ę  | Ą́  | Č  | É  | È  | Ė  | Ẽ  | Ì   | Í  | Į́  |
| D… | Š    | Į̃  | Ò  | Ó  | Ý  | Õ  | Ö  | Ũ  | Ų  | Ù  | Ú  | Ū  | Ü  | Ỹ   | Ž  | ß  |
| E… | ą    | į  | à  | á  | ä  | ã  | ę  | ą́  | č  | é  | è  | ė  | ẽ  | i̇̀   | i̇́  | į̇́  |
| F… | š    | į̇̃  | ò  | ó  | ý  | õ  | ö  | ũ  | ų  | ù  | ú  | ū  | ü  | ỹ   | ž  | ų̃  |
</div>

### LST 1590

**_Lietuvos standartas LST 1590. Informacijos technologija. Ženklų kodavimas 8 bitais_**

Šis standartas apibrėžia ženklų rinkinius, turinčius lietuviškus rašto ženklus, ir jų kodavimą atskirose operacinėse sistemose.
Jį sudaro atskiros dalys, kurių kiekviena dalis apibrėžia kodų lentelę pagrindinei arba kirčiuotų raidžių lietuvų kalbos abėcėlei, skirtą konkrečios genties operacinėms sistemoms.
Standartas yra atviras, t. y. teoriškai gali būti papildomas naujomis dalimis. Praktikoje nuo 2000 metų jis jokių papildymų nesusilaukė.
Standartą sudaro keturios dalys.

#### LST 1590-1 (DOS 775)

**_Lietuvos standartas LST 1590-1. Informacijos technologija. Ženklų kodavimas 8 bitais. 1 dalis. Grafinių ženklų rinkinys DOS terpei._**
Standartas apibrėžia lotynų 7-osios abėcėlės (Latin 7) ženklų rinkinį (tą patį, kurį apibrėžia pagrindinis standartas LST ISO/IEC 8859-13), papildytą operacinei sistemai DOS būdingais pseudografikos ženklais ir perrikiuotą, priderinant prie šios operacinės sistemos kodavimo sistemos savitumų.
Šio standarto apibrėžiamas kodavimas žinomas [kodų lentelės 775][LST 1590-1 vaizdas] vardu.

Šios kodų lentelės aukštesnioji pusė atrodo taip:
<div style="font-size:150%">

|    | …0  | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D | …E | …F   |
|----|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|------|
| 8… | Ć   | ü  | é  | ā  | ä  | ģ  | å  | ć  | ł  | ē  | Ŗ  | ŗ  | ī  | Ź  | Ä  | Å    |
| 9… | É   | æ  | Æ  | ō  | ö  | Ģ  | ¢  | Ś  | ś  | Ö  | Ü  | ø  | £  | Ø  | ×  | ¤    |
| A… | Ā   | Ī  | ó  | Ż  | ż  | ź  | ”  | ¦  | ©  | ®  | ¬  | ½  | ¼  | Ł  | «  | »    |
| B… | ░   | ▒  | ▓  | │  | ┤  | Ą  | Č  | Ę  | Ė  | ╣  | ║  | ╗  | ╝  | Į  | Š  | ┐    |
| C… | └   | ┴  | ┬  | ├  | ─  | ┼  | Ų  | Ū  | ╚  | ╔  | ╩  | ╦  | ╠  | ═  | ╬  | Ž    |
| D… | ą   | č  | ę  | ė  | į  | š  | ų  | ū  | ž  | ┘  | ┌  | █  | ▄  | ▌  | ▐  | ▀    |
| E… | Ó   | ß  | Ō  | Ń  | õ  | Õ  | µ  | ń  | Ķ  | ķ  | Ļ  | ļ  | ņ  | Ē  | Ņ  | ’    |
| F… | SHY | ±  | “  | ¾  | ¶  | §  | ÷  | „  | °  | ∙  | ·  | ¹  | ³  | ²  | ■  | NBSP |
</div>

#### LST 1590-2 (DOS 778)

**_Lietuvos standartas LST 1590-2. Informacijos technologija. Ženklų kodavimas 8 bitais. 2 dalis. Lietuviškų kirčiuotų raidžių ir transkripcijos ženklų rinkinys DOS terpei._**
Šis standartas apibrėžia DOS skirtą kodų lentelę, kurioje pagrindinės lietuvių kalbos abėcėlės raidžių aibė papildyta kirčiuotomis raidėmis bei fonetiniais ženklais.
Šioje kodų lentelėje pagrindinių (nekirčiuotų) lietuviškos abėcėlės raidžių ir kitų ženklų kodai sutampa su standarto LST 1590-1 kodais.
Ši kodų lentelė taip pat buvo žinoma [778][LST 1590-2 vaizdas] vardu.

Šios kodų lentelės aukštesnioji pusė atrodo taip:
<div style="font-size:150%">

|    | …0  | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D | …E | …F   |
|----|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|------|
| 8… | Á   | ü  | é  | à  | ä  | ẽ  | ã  | á  | ù  | ą́  | Ė̃  | ė̃  | i̇́  | È  | Ä  | Ã    |
| 9… | É   | ū́  | Ū́  | ý  | ö  | Ẽ  | Ę́  | Ú  | ú  | Ö  | Ü  | ė́  | Ę̃  | Ė́  | Ũ  | i̇̃    |
| A… | À   | Í  | ó  | Ỹ  | ỹ  | è  | L̃  | M̃  | Ñ  | Ū̃  | Ų́  | Ų̃  | ų́  | Ù  | R̃  | r̃    |
| B… | ░   | ▒  | ▓  | │  | ɑ  | Ą  | Č  | Ę  | Ė  | ɔ  | ║  | ╗  | ╝  | Į  | Š  | ┐    |
| C… | └   | ə  | ɛ  | ɡ  | ─  | ɪ  | Ų  | Ū  | ╚  | ╔  | ŋ  | θ  | ʃ  | ═  | ʊ  | Ž    |
| D… | ą   | č  | ę  | ė  | į  | š  | ų  | ū  | ž  | ┘  | ┌  | ´  | ʌ  | ʒ  | ˈ  | ˌ    |
| E… | Ó   | ß  | Ý  | Į̃  | õ  | Õ  | l̃  | į̇̃  | Ì  | i̇̀  | Į́  | į̇́  | ò  | Ą́  | Ò  | ų̃    |
| F… | SHY | ą̃  | “  | ū̃  | Ą̃  | m̃  | ũ  | „  | Ĩ  | æ  | ð  | ñ  | ę̃  | ę́  | j̇̃  | NBSP |
</div>

#### LST 1590-3 (Windows-1257)

**_Lietuvos standartas LST 1590-3. Informacijos technologija. Ženklų kodavimas 8 bitais. 3 dalis. Grafinių ženklų rinkinys „Windows“ terpei._**
Standartas apibrėžia aštuonbitę kodų lentelę su lietuviškomis raidėmis „Windows“ genties operacinėse sistemose.
Jo apibrėžiama kodų lentelė plačiau žinoma [1257][LST 1590-3 vaizdas] vardu.
Šioje lentelėje visų lietuviškos abėcėlės raidžių kodai sutampa su standarto LST ISO/IEC 8859-13 apibrėžiamais kodais.
Skiriasi tik 4 skyrybos ženklų (kabučių ir apostrofo) kodavimas, atsiradęs dėl savitų „Microsoft“ kodavimo principų.

Aukštesnioji šios kodų lentelės pusė atrodo taip:
<div style="font-size:150%">

|    | …0   | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D  | …E | …F |
|----|------|----|----|----|----|----|----|----|----|----|----|----|----|-----|----|----|
| 8… | €    |    | ‚  |    | „  | …  | †  | ‡  |    | ‰  |    | ‹  |    | ¨   | ˇ  | ¸  |
| 9… |      | ‘  | ’  | “  | ”  | •  | –  | —  |    | ™  |    | ›  |    | ¯   | ˛  |    |
| A… | NBSP |    | ¢  | £  | ¤  |    | ¦  | §  | Ø  | ©  | Ŗ  | «  | ¬  | SHY | ®  | Æ  |
| B… | °    | ±  | ²  | ³  | ´  | µ  | ¶  | ·  | ø  | ¹  | ŗ  | »  | ¼  | ½   | ¾  | æ  |
| C… | Ą    | Į  | Ā  | Ć  | Ä  | Å  | Ę  | Ē  | Č  | É  | Ź  | Ė  | Ģ  | Ķ   | Ī  | Ļ  |
| D… | Š    | Ń  | Ņ  | Ó  | Ō  | Õ  | Ö  | ×  | Ų  | Ł  | Ś  | Ū  | Ü  | Ż   | Ž  | ß  |
| E… | ą    | į  | ā  | ć  | ä  | å  | ę  | ē  | č  | é  | ź  | ė  | ģ  | ķ   | ī  | ļ  |
| F… | š    | ń  | ņ  | ó  | ō  | õ  | ö  | ÷  | ų  | ł  | ś  | ū  | ü  | ż   | ž  | ˙  |
</div>

#### LST 1590-4

**_Lietuvos standartas LST 1590-4. Informacijos technologija. Ženklų kodavimas 8 bitais. 4 dalis. Lietuviškų kirčiuotų raidžių ir transkripcijos ženklų rinkinys „Windows“ terpei._**
Šis standartas apibrėžia [kodų lentelę][LST 1590-4 vaizdas], kurioje pagrindinės lietuvių kalbos abėcėlės raidžių aibė papildyta kirčiuotomis raidėmis bei fonetiniais ženklais.
Šioje kodų lentelėje pagrindinių (nekirčiuotų) lietuviškos abėcėlės raidžių ir visų kitų ženklų, išskyrus kirčiuotas raides ir fonetinius ženklus, kodai sutampa su standarto LST 1590-3 kodais.

Šios kodu lentelės aukštesnioji pusė atrodo taip:
<div style="font-size:150%">

|    | …0   | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D  | …E | …F |
|----|------|----|----|----|----|----|----|----|----|----|----|----|----|-----|----|----|
| 8… | €    |    | ɑ  | ɔ  | „  | ə  | ɛ  | ɡ  | ɪ  | ŋ  | θ  | ˈ  | ʃ  |     |    |    |
| 9… |      | ‘  | ’  | “  | ”  | •  | –  | —  | ʊ  | ʌ  | ʒ  | ˌ  | æ  |     |    | ð  |
| A… | NBSP | Ą̃  | Ę́  | Ę̃  | i̇̃  | L̃  | M̃  | m̃  | Ė́  | Ñ  | Ė̃  | R̃  | Ų́  | SHY | Ū̃  | Ū́  |
| B… | Ĩ    | ą̃  | ę́  | ę̃  | ´  | l̃  | ¶  | j̇̃  | ė́  | ñ  | ė̃  | r̃  | ų́  | Ų̃   | ū̃  | ū́  |
| C… | Ą    | Į  | À  | Á  | Ä  | Ã  | Ę  | Ą́  | Č  | É  | È  | Ė  | Ẽ  | Ì   | Í  | Į́  |
| D… | Š    | Į̃  | Ò  | Ó  | Ý  | Õ  | Ö  | Ũ  | Ų  | Ù  | Ú  | Ū  | Ü  | Ỹ   | Ž  | ß  |
| E… | ą    | į  | à  | á  | ä  | ã  | ę  | ą́  | č  | é  | è  | ė  | ẽ  | i̇̀   | i̇́  | į̇́  |
| F… | š    | į̇̃  | ò  | ó  | ý  | õ  | ö  | ũ  | ų  | ù  | ú  | ū  | ü  | ỹ   | ž  | ų̃  |
</div>

### Senesnės 8 bitų koduotės

Aukščiau išvardintos 8 bitų koduotės Lietuvoje standartizuotos 2000 metais.
Žemiau išvardintos kitos 8 bitų koduotės, naudotos kai kuriose terpėse.
Dalis jų apskritai nebuvo standartizuotos, kitų standartai (išskyrus ISO/IEC 8859-4) 2000 metais panaikinti.

Informacija apie daugumą šių lentelių surinkta iš UAB „Fotonija“ svetainės ir LIKIT svetainės archyvinių kopijų.

#### ISO/IEC 8859-4

**_Lietuvos TSR RST 1093–89: Informacijos apdorojimo sistema. Daugiakalbis koduotų ženklų rinkinys su lietuviškomis raidėmis. Aštuonių bitų kodai._**

ISO/IEC 8859 standartų šeimoje lietuvių kalbai iš pradžių buvo numatyta [ISO/IEC 8859-4][ISO 8859-4 vaizdas] koduotė, skirta Šiaurės Europos ir Baltijos šalims.
Deja, dėl didelio raidžių skaičiaus joje neliko vietos kai kuriems skyrybos ženklams, tokiems, kaip figūrinės kabutės ar brūkšnys, tad lietuviškiems tekstams ji buvo tinkama tik su išlygomis.
Lietuvos standartas numatė, jog simbolį, kurio kodas 184 (B8) leidžiama keisti lietuviškomis atidarančiosiomis kabutėmis.
1992 m. šis standartas pakeistas, priėmus LST 1282, vėliau tapusį ISO 8859-13.

Aukštesnioji šios kodų lentelės pusė (128-255 pozicijos) atrodo taip:

<div style="font-size:150%">

|    | …0   | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D  | …E | …F |
|----|------|----|----|----|----|----|----|----|----|----|----|----|----|-----|----|----|
| 8… |      |    |    |    |    |    |    |    |    |    |    |    |    |     |    |    |
| 9… |      |    |    |    |    |    |    |    |    |    |    |    |    |     |    |    |
| A… | NBSP | Ą  | ĸ  | Ŗ  | ¤  | Ĩ  | Ļ  | §  | ¨  | Š  | Ē  | Ģ  | Ŧ  | SHY | Ž   | ¯  |
| B… | °    | ą  | ˛  | ŗ  | ´  | ĩ  | ļ  | ˇ  | ¸  | š  | ē  | ģ  | ŧ  | Ŋ   | ž   | ŋ  |
| C… | Ā    | Á  | Â  | Ã  | Ä  | Å  | Æ  | Į  | Č  | É  | Ę  | Ë  | Ė  | Í   | Î   | Ī  |
| D… | Đ    | Ņ  | Ō  | Ķ  | Ô  | Õ  | Ö  | ×  | Ø  | Ų  | Ú  | Û  | Ü  | Ũ   | Ū   | ß  |
| E… | ā    | á  | â  | ã  | ä  | å  | æ  | į  | č  | é  | ę  | ë  | ė  | í   | î   | ī  |
| F… | đ    | ņ  | ō  | ķ  | ô  | õ  | ö  | ÷  | ø  | ų  | ú  | û  | ü  | ũ   | ū   | ˙  |
</div>

#### ISO/IEC 8859-10

Ši koduotė skirta Šiaurės šalims, tačiau joje taipogi yra visos lietuviškos raidės.
Visgi, kaip ir ISO/IEC 8859-4 koduotėje, čia nėra nei lietuviškų kabučių, nei brūkšnio, tad mums ji nebuvo nė kiek geresnė.
Lietuvoje ši koduotė niekada nebuvo standartizuota.

Aukštesnioji šios kodų lentelės pusė (128-255 pozicijos) atrodo taip:

<div style="font-size:150%">

|    | …0   | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D   | …E | …F |
|----|------|----|----|----|----|----|----|----|----|----|----|----|----|------|----|----|
| 8… |      |    |    |    |    |    |    |    |    |    |    |    |    |      |    |    |
| 9… |      |    |    |    |    |    |    |    |    |    |    |    |    |      |    |    |
| A… | NBSP | Ą  | Ē  | Ģ  | Ī  | Ĩ  | Ķ  | §  | Ļ  | Đ  | Š  | Ŧ  | Ž  | ­SHY | Ū  | Ŋ  |
| B… | °    | ą  | ē  | ģ  | ī  | ĩ  | ķ  | ·  | ļ  | đ  | š  | ŧ  | ž  | ―    | ū  | ŋ  |
| C… | Ā    | Á  | Â  | Ã  | Ä  | Å  | Æ  | Į  | Č  | É  | Ę  | Ë  | Ė  | Í    | Î  | Ï  |
| D… | Ð    | Ņ  | Ō  | Ó  | Ô  | Õ  | Ö  | Ũ  | Ø  | Ų  | Ú  | Û  | Ü  | Ý    | Þ  | ß  |
| E… | ā    | á  | â  | ã  | ä  | å  | æ  | į  | č  | é  | ę  | ë  | ė  | í    | î  | ï  |
| F… | ð    | ņ  | ō  | ó  | ô  | õ  | ö  | ũ  | ø  | ų  | ú  | û  | ü  | ý    | þ  | ĸ  |

</div>


#### DOS 770 (LST 1095)

**_LST 1095-89 Informacijos apdorojimo sistema. Personalinių kompiuterių ženklų rinkinys su lietuviškomis raidėmis.
Aštuonių bitų kodai._**

Tai – pirmoji standartizuota Baltijos šalių koduotė DOS sistemai.
Koduotė geriau žinoma kaip [DOS 770][DOS 770 vaizdas], pat vadinta „IBM Baltic“ vardu.
Ankstesnis šio standarto žymuo – RST 1095-89.
Jį parengė Virginijus Dadurkevičius, Danielius Ralys, Julius Sruogis ir Rimas Voldemaras konsultuodamiesi su latviais ir estais.

Aukštesnioji šios kodų lentelės pusė (128-255 pozicijos) atrodo taip:

<div style="font-size:150%">

|    | …0 | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D | …E | …F   |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|------|
| 8… | Č  | ü  | ė  | ā  | ä  | ą  | ļ  | č  | ē  | Ē  | ę  | Ę  | ī  | į  | Ä  | Ą    |
| 9… | Ė  | ž  | Ž  | õ  | ö  | Õ  | ū  | ų  | ģ  | Ö  | Ü  | ¢  | Ļ  | „  | š  | Š    |
| A… | Ā  | Ī  | ķ  | Ķ  | ņ  | Ņ  | Ū  | Ų  | Ģ  | ⌐  | ¬  | ½  | ¼  | Į  | «  | »    |
| B… | ░  | ▒  | ▓  | │  | ┤  | ╡  | ╢  | ╖  | ╕  | ╣  | ║  | ╗  | ╝  | ╜  | ╛  | ┐    |
| C… | └  | ┴  | ┬  | ├  | ─  | ┼  | ╞  | ╟  | ╚  | ╔  | ╩  | ╦  | ╠  | ═  | ╬  | ╧    |
| D… | ╨  | ╤  | ╥  | ╙  | ╘  | ╒  | ╓  | ╫  | ╪  | ┘  | ┌  | █  | ▄  | ▌  | ▐  | ▀    |
| E… | α  | ß  | Γ  | π  | Σ  | σ  | µ  | τ  | Φ  | Θ  | Ω  | δ  | ∞  | φ  | ε  | ∩    |
| F… | ≡  | ±  | ≥  | ≤  | ⌠  | ⌡  | ÷  | ≈  | °  | ∙  | ·  | √  | ⁿ  | ²  | ■  | NBSP |
</div>

#### DOS 771 (KBL)

Kone seniausiai DOS terpėje Lietuvoje naudota [kodų lentelė][DOS 771 vaizdas], apimanti rusų ir lietuvių kalbų rašmenis (išskyrus rusišką raidę **Ёё**).
Šios koduotės autorius – Vidmantas Balčytis.
Rusų abėcėlės raidės joje išdėstytose tose pačiose vietose, kaip ir kirilicai skirtoje DOS 866 koduotėje, ir užima visas vietas, kurias buvo įprasta skirti nacionalinėms raidėms.
Lietuviškos raidės buvo išdėstytos vietoj pseudografikos bei matematinių ženklų.
Tai kėlė nemažai problemų, tačiau ši koduotė buvo gan populiari, nes ją į kompiuterius dažnai diegdavo pardavėjai.

Aukštesnioji šios kodų lentelės pusė:

<div style="font-size:150%">

|    | …0 | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D | …E | …F   |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|------|
| 8… | А  | Б  | В  | Г  | Д  | Е  | Ж  | З  | И  | Й  | К  | Л  | М  | Н  | О  | П    |
| 9… | Р  | С  | Т  | У  | Ф  | Х  | Ц  | Ч  | Ш  | Щ  | Ъ  | Ы  | Ь  | Э  | Ю  | Я    |
| A… | а  | б  | в  | г  | д  | е  | ж  | з  | и  | й  | к  | л  | м  | н  | о  | п    |
| B… | ░  | ▒  | ▓  | │  | ┤  | ╡  | ╢  | ╖  | ╕  | ╣  | ║  | ╗  | ╝  | ╜  | ╛  | ┐    |
| C… | └  | ┴  | ┬  | ├  | ─  | ┼  | ╞  | ╟  | ╚  | ╔  | ╩  | ╦  | ╠  | ═  | ╬  | ╧    |
| D… | ╨  | ╤  | ╥  | ╙  | ╘  | ╒  | ╓  | ╫  | ╪  | ┘  | ┌  | █  | Ą  | ą  | Č  | č    |
| E… | р  | с  | т  | у  | ф  | х  | ц  | ч  | ш  | щ  | ъ  | ы  | ь  | э  | ю  | я    |
| F… | Ę  | ę  | Ė  | ė  | Į  | į  | Š  | š  | Ų  | ų  | Ū  | ū  | Ž  | ž  | ■  | NBSP |
</div>

#### DOS 772 (LST 1284)

**_LST 1284:1993 Informacijos technologija. 8 bitų lotyniškos abėcėlės koduotų ženklų rinkinys, papildytas lietuviškos ir
rusiškos abėcėlių raidėmis, skirtas naudoti MS DOS aplinkoje. 772 kodų lentelė._**

Ši koduotė taipogi pirmenybę teikė rusiškoms raidėms: jos joje irgi išdėstytos tose pačiose vietose, kaip ir DOS 866 koduotėje.
Nuo 771 koduotės ši skiriasi lietuviškų raidžių pozicijomis.
Joje „paaukoti“ ne lentelės pabaigoje buvę matematiniai ženklai, o pseudografikos dvigubų ir viengubų linijų sankirtos.
Tai vis tiek kėlė problemų, tačiau bent jau pseudografiką naudojančios programos nebuvo per daug išdarkomos.
Lietuviškų raidžių vietos šioje [kodų lentelėje][DOS 772 vaizdas] sutampa su 775 kodų lentele (LST 1590-1).
Joje yra abejos lietuviškos figūrinės kabutės.
Ši koduotė taip pat kartais vadinama 1119 numeriu.
Šis standartas nuo 2000 m. panaikintas.

Aukštesnioji šios kodų lentelės pusė:

<div style="font-size:150%">

|    | …0 | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D | …E | …F   |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|------|
| 8… | А  | Б  | В  | Г  | Д  | Е  | Ж  | З  | И  | Й  | К  | Л  | М  | Н  | О  | П    |
| 9… | Р  | С  | Т  | У  | Ф  | Х  | Ц  | Ч  | Ш  | Щ  | Ъ  | Ы  | Ь  | Э  | Ю  | Я    |
| A… | а  | б  | в  | г  | д  | е  | ж  | з  | и  | й  | к  | л  | м  | н  | о  | п    |
| B… | ░  | ▒  | ▓  | │  | ┤  | Ą  | Č  | Ę  | Ė  | ╣  | ║  | ╗  | ╝  | Į  | Š  | ┐    |
| C… | └  | ┴  | ┬  | ├  | ─  | ┼  | Ų  | Ū  | ╚  | ╔  | ╩  | ╦  | ╠  | ═  | ╬  | Ž    |
| D… | ą  | č  | ę  | ė  | į  | š  | ų  | ū  | ž  | ┘  | ┌  | █  | ▄  | ▌  | ▐  | ▀    |
| E… | р  | с  | т  | у  | ф  | х  | ц  | ч  | ш  | щ  | ъ  | ы  | ь  | э  | ю  | я    |
| F… | Ё  | ё  | ≥  | ≤  | „  | “  | ÷  | ≈  | °  | ∙  | ·  | √  | ⁿ  | ²  | ■  | NBSP |
</div>

#### DOS 773

Lietuviškų raidžių išdėstymas [šioje kodų lentelėje][DOS 773 vaizdas] atitinka KBL išdėstymą, tačiau rusiškų raidžių joje nėra,
nes ženklų aibė sutampa su 775 kodų lentele.

Aukštesnioji šios kodų lentelės pusė:

<div style="font-size:150%">

|    | …0 | …1 | …2 | …3 | …4 | …5 | …6 | …7  | …8 | …9 | …A | …B | …C | …D | …E | …F   |
|----|----|----|----|----|----|----|----|-----|----|----|----|----|----|----|----|------|
| 80 | Ć  | ü  | é  | ā  | ä  | ģ  | å  | ć   | ł  | ē  | Ŗ  | ŗ  | ī  | Ź  | Ä  | Å    |
| 90 | É  | æ  | Æ  | ō  | ö  | Ģ  | ¢  | Ś   | ś  | Ö  | Ü  | ø  | £  | Ø  | ×  | ¤    |
| a0 | Ā  | Ī  | ó  | Ż  | ż  | ź  | ”  | ¦   | ©  | ®  | ¬  | ½  | ¼  | Ł  | «  | »    |
| b0 | ░  | ▒  | ▓  | │  | ┤  | ±  | ╢  | “   | ¾  | ╣  | ║  | ╗  | ╝  | ¶  | §  | ┐    |
| c0 | └  | ┴  | ┬  | ├  | ─  | ┼  | ÷  | ╟   | ╚  | ╔  | ╩  | ╦  | ╠  | ═  | ╬  | ╧    |
| d0 | °  | ╤  | ∙  | ·  | ¹  | „  | ³  | SHY | ²  | ┘  | ┌  | █  | Ą  | ą  | Č  | č    |
| e0 | Ó  | ß  | Ō  | Ń  | õ  | Õ  | µ  | ń   | Ķ  | ķ  | Ļ  | ļ  | ņ  | Ē  | Ņ  | ’    |
| f0 | Ę  | ę  | Ė  | ė  | Į  | į  | Š  | š   | Ų  | ų  | Ū  | ū  | Ž  | ž  | ■  | NBSP |
</div>

#### DOS 774 (LST 1283)

**_LST 1283:1993 Informacijos technologija. 8 bitų lotyniškos abėcėlės koduotų ženklų rinkinys, papildytas lietuviškos
abėcėlės raidėmis, skirtas naudoti MS DOS aplinkoje. 774 kodų lentelė._**

[Šioje koduotėje][DOS 774 vaizdas] lietuviškų raidžių pozicijos sutampa su 772 koduote, tačiau vietoj rusiškų raidžių yra pateiktas įvairių Europos kalbų raidžių rinkinys.
Vėliau standartizuota 775 koduotė nuo šios skiriasi tuo, kad joje ką tik minėtos raidės pakeistos naudojamomis latvių ir estų kalbose.

Šis standartas nuo 2000 m. panaikintas.

Aukštesnioji kodų lentelės pusė:

<div style="font-size:150%">

|    | …0 | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D | …E | …F   |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|------|
| 8… | Ç  | ü  | é  | â  | ä  | à  | å  | ç  | ê  | ë  | è  | ï  | î  | ì  | Ä  | Å    |
| 9… | É  | æ  | Æ  | ô  | ö  | ò  | û  | ù  | ÿ  | Ö  | Ü  | ¢  | £  | ¥  | ₧  | ƒ    |
| A… | á  | í  | ó  | ú  | ñ  | Ñ  | ª  | º  | ¿  | ⌐  | ¬  | ½  | ¼  | ¡  | «  | »    |
| B… | ░  | ▒  | ▓  | │  | ┤  | Ą  | Č  | Ę  | Ė  | ╣  | ║  | ╗  | ╝  | Į  | Š  | ┐    |
| C… | └  | ┴  | ┬  | ├  | ─  | ┼  | Ų  | Ū  | ╚  | ╔  | ╩  | ╦  | ╠  | ═  | ╬  | Ž    |
| D… | ą  | č  | ę  | ė  | į  | š  | ų  | ū  | ž  | ┘  | ┌  | █  | ▄  | ▌  | ▐  | ▀    |
| E… | α  | ß  | Γ  | π  | Σ  | σ  | µ  | τ  | Φ  | Θ  | Ω  | δ  | ∞  | φ  | ε  | ∩    |
| F… | ≡  | ±  | ≥  | ≤  | „  | “  | ÷  | ≈  | °  | ∙  | ·  | √  | ⁿ  | ²  | ■  | NBSP |
</div>

#### DOS 776

[Kodų lentelė][DOS 776 vaizdas], sudaryta papildant 770 lentelę lietuviškomis kirčiuotomis raidėmis ir žodynuose naudojamais
ženklais.
Aukštesnioji šios kodų lentelės pusė atrodo taip:

<div style="font-size:150%">

|    | …0 | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D | …E | …F   |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|------|
| 8… | Č  | ü  | ė  | ã  | ä  | ą  | ļ  | č  | ẽ  | Ẽ  | ę  | Ę  | i̇̃  | į  | Ä  | Ą    |
| 9… | Ė  | ž  | Ž  | õ  | ö  | Õ  | ū  | ų  | ỹ  | Ö  | Ü  | m̃  | l̃  | „  | š  | Š    |
| A… | Ã  | Ĩ  | ó  | ú  | ņ  | Ñ  | Ū  | Ų  | Ỹ  | “  | ñ  | M̃  | L̃  | Į  | «  | »    |
| B… | À  | Á  | Ą́  | │  | Ą̃  | È  | É  | Ę́  | Ę̃  | Ė́  | ║  | ╗  | ╝  | Ė̃  | Ì  | ┐    |
| C… | └  | Í  | Į́  | Į̃  | ─  | Ý  | Ò  | Ó  | ╚  | ╔  | R̃  | Ù  | Ú  | ═  | Ũ  | Ų́    |
| D… | Ų̃  | Ū́  | Ū̃  | à  | á  | ą́  | ą̃  | è  | é  | ┘  | ┌  | ę́  | ę̃  | ė́  | ė̃  | i̇̀    |
| E… | α  | ß  | i̇́  | į̇́  | į̇̃  | ý  | ò  | r̃  | ù  | θ  | ũ  | ð  | ų́  | ų̃  | ε  | ū́    |
| F… | ū̃  | ɪ  | æ  | ɔ  | ʊ  | ʌ  | ə  | ʃ  | ʒ  | m̦  | ŋ  | ŗ  | ɡ  |    | ˈ  | NBSP |
</div>

#### DOS 777

[Kodų lentelė][DOS 777 vaizdas], sudaryta papildant 771 lentelę lietuviškomis kirčiuotomis raidėmis ir ženklais naudojamais
žodynų sudarymui.
Aukštesnioji šios kodų lentelės pusė:

<div style="font-size:150%">

|    | …0 | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D | …E | …F   |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|------|
| 8… | Á  | ü  | é  | à  | ä  | ẽ  | ã  | á  | ù  | ą́  | Ė̃  | ė̃  | i̇́  | È  | Ä  | Ã    |
| 9… | É  | ū́  | Ū́  | ý  | ö  | Ẽ  | Ę́  | Ú  | ú  | Ö  | Ü  | ė́  | Ę̃  | Ė́  | Ũ  | i̇̃    |
| A… | À  | Í  | ó  | Ỹ  | ỹ  | è  | L̃  | M̃  | Ñ  | Ū̃  | Ų́  | Ų̃  | ų́  | Ù  | R̃  | r̃    |
| B… | ░  | ▒  | ▓  | │  | ɑ  | ą̃  | ʌ  | “  | ū̃  | ɔ  | ║  | ╗  | ╝  | Ą̃  | m̃  | ┐    |
| C… | └  | ə  | ɛ  | ɡ  | ─  | ɪ  | ũ  | ʒ  | ╚  | ╔  | ŋ  | θ  | ʃ  | ═  | ʊ  | ˈ    |
| D… | Ĩ  | ˌ  | æ  | ð  | ñ  | „  | ę̃  | SHY | ę́  | ┘  | ┌  | █  | Ą  | ą  | Č  | č    |
| E… | Ó  | ß  | Ý  | Į̃  | õ  | Õ  | Ĩ  | į̇̃  | Ì  | i̇̀  | Į́  | į̇́  | ò  | Ą́  | Ò  | ų̃    |
| F… | Ę  | ę  | Ė  | ė  | Į  | į  | Š  | š  | Ų  | ų  | Ū  | ū  | Ž  | ž  | ■  | NBSP |
</div>

#### 10029 (MacCE)

Vidurio Europos ir Baltijos šalims skirta senųjų „Mac OS” operacinės sistemos [10029 kodų lentelė][MacCE vaizdas].
Aukštesnioji lentelės pusė:

<div style="font-size:150%">

|    | …0 | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A   | …B | …C | …D | …E | …F |
|----|----|----|----|----|----|----|----|----|----|----|------|----|----|----|----|----|
| 8… | Ä  | Ā  | ā  | É  | Ą  | Ö  | Ü  | á  | ą  | Č  | ä    | č  | Ć  | ć  | é  | Ź  |
| 9… | ź  | Ď  | í  | ď  | Ē  | ē  | Ė  | ó  | ė  | ô  | ö    | õ  | ú  | Ě  | ě  | ü  |
| A… | †  | °  | Ę  | £  | §  | •  | ¶  | ß  | ®  | ©  | ™    | ę  | ¨  | ≠  | ģ  | Į  |
| B… | į  | Ī  | ≤  | ≥  | ī  | Ķ  | ∂  | ∑  | ł  | Ļ  | ļ    | Ľ  | ľ  | Ĺ  | ĺ  | Ņ  |
| C… | ņ  | Ń  | ¬  | √  | ń  | Ň  | ∆  | «  | »  | …  | NBSP | ň  | Ő  | Õ  | ő  | Ō  |
| D… | –  | —  | “  | ”  | ‘  | ’  | ÷  | ◊  | ō  | Ŕ  | ŕ    | Ř  | ‹  | ›  | ř  | Ŗ  |
| E… | ŗ  | Š  | ‚  | „  | š  | Ś  | ś  | Á  | Ť  | ť  | Í    | Ž  | ž  | Ū  | Ó  | Ô  |
| F… | ū  | Ů  | Ú  | ů  | Ű  | ű  | Ų  | ų  | Ý  | ý  | ķ    | Ż  | Ł  | ż  | Ģ  | ˇ  |
</div>

#### Spectrum

Pirmoji plačiau naudota lietuviška [kodų lentelė][Spectrum vaizdas] „Windows“ terpei.
Ši koduotė nebuvo standartizuota.
Žvelgiant į lentelę, panašu, kad ši koduotė buvo sukurta, tiesiog pakeitus po devynias mažąsias ir didžiąsias raides ISO/IEC 8859-1 koduotėje ir pridėjus du viengubų figūrinių kabučių ženklus.
Kaip ir kelios kitos atskirų vietinių įmonių sukurtos koduotės, „Spectrum“ nespėjo labai paplisti – jas visas greitai išstūmė „Windows-1257“.

Aukštesnioji lentelės pusė:

<div style="font-size:150%">

|    | …0   | …1 | …2 | …3 | …4 | …5 | …6 | …7 | …8 | …9 | …A | …B | …C | …D | …E | …F |
|----|------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 8… |      |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| 9… |      | ‘  | ’  |    |    |    |    |    |    |    |    |    |    |    |    |    |
| A… | NBSP | ¡  | ¢  | £  | ¤  | ¥  | ¦  | §  | ¨  | ©  | ª  | «  | ¬  | SHY | ®  | ¯  |
| B… | °    | ±  | ²  | ³  | ´  | µ  | ¶  | ·  | ¸  | ¹  | º  | »  | ¼  | ½  | ¾  | ¿  |
| C… | Ą    | Á  | Â  | Ã  | Ä  | Å  | Č  | Ç  | Ę  | Ė  | Ê  | Ë  | Į  | Í  | Î  | Ï  |
| D… | Ð    | Ñ  | Ò  | Ó  | Ô  | Õ  | Š  | ×  | Ø  | Ų  | Ū  | Ž  | Ü  | Ý  | Þ  | ß  |
| E… | ą    | á  | â  | ã  | ä  | å  | č  | ç  | ę  | ė  | ê  | ë  | į  | í  | î  | ï  |
| F… | ð    | ñ  | ò  | ó  | ô  | õ  | š  | ÷  | ø  | ų  | ū  | ž  | ü  | ý  | þ  | ÿ  |
</div>

### BALTIC EBCDIC (1112 ir 1156)

EBCDIC grupės koduotės yra skirtos „didiesiems“ kompiuteriams (angl. _mainframe_) ir įprastame vartojime praktiškai nesutinkama.
[1112 kodų lentelė][BALTIC EBCDIC vaizdas] nuo 1156 skiriasi tik viena pozicija: 1112 lentelėje 9F pozicijoje yra bendrinis valiutos ženklas (¤), o atnaujintoje 1156 lentelėje – euro ženklas (€).
1112 kodų lentelė apibrėžta Latvijos standarte RST 0040-90.
Panašu, kad Lietuvoje ji standartizuota nebuvo.

EBCDIC koduotės sudarytos kitu principu, nei ASCII pagrindo koduotės, todėl žemiau 1156 koduotės lentelė pateikiama visa apimtimi:

<div style="font-size:150%">

|    | …0  | …1   | …2  | …3  | …4  | …5 | …6  | …7  | …8  | …9   | …A  | …B  | …C | …D | …E | …F  |
|----|-----|------|-----|-----|-----|----|-----|-----|-----|------|-----|-----|----|----|----|-----|
| 0… | ␀   | ␁    | ␂   | ␃   | ST  | ␉  | SSA | ␡   | SSA | RI   | SS2 | ␋   | ␌  | ␍  | ␎  | ␏   |
| 1… | ␐   | ␑    | ␒   | ␓   | OSC | NL | ␈   | ESA | ␘   | ␙    | PU2 | SS3 | ␜  | ␝  | ␞  | ␟   |
| 2… | PAD | HOP  | BPH | NBH | IND | ␊  | ␗   | ␛   | HTS | HTJ  | VTS | PLD | UP | ␅  | ␆  | ␇   |
| 3… | DCS | PU1  | ␖   | STS | CCH | MW | SPA | ␄   | SOS | SGCI | SCI | CSI | ␔  | ␕  | PM | ␚   |
| 4… | ␠   | NBSP | š   | ä   | ą   | į  | ū   | å   | ē   | ž    | ¢   | .   | <  | (  | +  | \!  |
| 5… | &   | é    | ę   | ė   | č   | ų  | „   | “   | ģ   | ß    | !   | $   | *  | )  | ;  | ¬   |
| 6… | -   | /    | Š   | Ä   | Ą   | Į  | Ū   | Å   | Ē   | Ž    | ¦   | ,   | %  | _  | >  | ?   |
| 7… | ø   | É    | Ę   | Ė   | Č   | Ų  | Ī   | Ļ   | Ģ   | `    | :   | #   | @  | '  | =  | "   |
| 8… | Ø   | a    | b   | c   | d   | e  | f   | g   | h   | i    | «   | »   | ā  | ż  | ń  | ±   |
| 9… | °   | j    | k   | l   | m   | n  | o   | p   | q   | r    | Ŗ   | ŗ   | æ  | ķ  | Æ  | €   |
| A… | µ   | ~    | s   | t   | u   | v  | w   | x   | y   | z    | ”   | ź   | Ā  | Ż  | Ń  | ®   |
| B… | ^   | £    | ī   | ·   | ©   | §  | ¶   | ¼   | ½   | ¾    | [   | ]   | Ź  | Ķ  | ļ  | ×   |
| C… | {   | A    | B   | C   | D   | E  | F   | G   | H   | I    | SHY | ō   | ö  | ņ  | ó  | õ   |
| D… | }   | J    | K   | L   | M   | N  | O   | P   | Q   | R    | ¹   | ć   | ü  | ł  | ś  | ’   |
| E… | \   | ÷    | S   | T   | U   | V  | W   | X   | Y   | Z    | ²   | Ō   | Ö  | Ņ  | Ó  | Õ   |
| F… | 0   | 1    | 2   | 3   | 4   | 5  | 6   | 7   | 8   | 9    | ³   | Ć   | Ü  | Ł  | Ś  | APC |
</div>

Kaip ir aukščiau, šioje lentelėje nespausdinami ženklai žymimi jų grafiniam atvaizdavimui skirtais ženklais, o kai tokių Unikode nėra – įprastinėmis santrumpomis.

[Tarptautinė standartų organizacija]: https://www.iso.org/ "ISO – International Organization for Standardization – iso.org"
[„Unicode“ konsorciumas]: http://www.unicode.org/ "Unicode – The World Standard for Text and Emoji – unicode.org"
[Unikodo versijos]: https://www.unicode.org/versions/ "About Versions of the Unicode® Standard – The Unicode Standard – unicode.org"
[ISO 8859]: https://en.wikipedia.org/wiki/ISO/IEC_8859 "Informacija apie ISO/IEC 8859 standartą (anglų k.)"
[ISO 8859-4 vaizdas]: 8859-4.gif "Šiaurės Europos ir Baltijos šalims skirta ISO 8859-4 kodų lentelė (grafinis vaizdas)"
[ISO 8859-13 vaizdas]: 8859-13.gif "Baltijos šalims skirta ISO 8859-13 kodų lentelė (grafinis vaizdas)"
[LST 1564 vaizdas]: 1564.gif "Standarto LST 1564 lentelė (grafinis vaizdas)"
[LST 1590-1 vaizdas]: 1590-1.gif "775 kodų lentelė (standartas LST 1590-1; grafinis vaizdas)"
[LST 1590-2 vaizdas]: 1590-2.gif "778 kodų lentelė (standartas LST 1590-2; grafinis vaizdas)"
[LST 1590-3 vaizdas]: 1590-3.gif "1257 kodų lentelė (standartas LST 1590-3; grafinis vaizdas)"
[LST 1590-4 vaizdas]: 1590-4.gif "LST 1590-4 standarto kodų lentelė (grafinis vaizdas)"
[DOS 770 vaizdas]: 770.gif "DOS 770 kodų lentelė (grafinis vaizdas)"
[DOS 771 vaizdas]: 771.gif "DOS 771 (KBL) kodų lentelė (grafinis vaizdas)"
[DOS 772 vaizdas]: 772.gif "DOS 772 kodų lentelė (grafinis vaizdas)"
[DOS 773 vaizdas]: 773.gif "DOS 773 kodų lentelė (grafinis vaizdas)"
[DOS 774 vaizdas]: 774.gif "DOS 774 kodų lentelė (standartas LST 1283; grafinis vaizdas)"
[DOS 776 vaizdas]: 776.png "DOS 776 kodų lentelė (grafinis vaizdas)"
[DOS 777 vaizdas]: 777.gif "DOS 777 kodų lentelė (grafinis vaizdas)"
[MacCE vaizdas]: 10029-k.gif "„Mac OS Central European“ (10029) kodų lentelė (grafinis vaizdas)"
[Spectrum vaizdas]: spectrum.gif "„Spectrum“ kodų lentelė (grafinis vaizdas)"
[BALTIC EBCDIC vaizdas]: baltic-ebcdic.gif "BALTIC EBCDIC 1112 kodų lentelė (grafinis vaizdas)"
