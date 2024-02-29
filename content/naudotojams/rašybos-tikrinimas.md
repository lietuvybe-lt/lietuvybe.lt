---
title: Lietuviškos rašybos tikrinimo priemonės
linkTitle: Rašybos tikrinimas
type: page
aliases:
    - /naudotojams/rasybos-tikrinimas/
menu:
    main:
        weight: 10
        parent: Naudotojams
---

Rašybos tikrinimo žodynas „ispell-lt“
-------------------------------------

„ispell-lt“ yra lietuvių kalbos rašybos tikrinimo taisyklės ir žodynas įprastiniam UNIX rašybos tikrinimo įrankiui
[„Ispell“](https://www.cs.hmc.edu/~geoff/ispell.html). Iš tų pačių pradinių duomenų „ispell-lt“ projekte generuojami
ir [„Aspell“](http://aspell.net/), [„MySpell“](http://code.google.com/a/apache-extras.org/p/ooo-myspell/),
[„Hunspell“](https://hunspell.github.io/) bei [„Nuspell“](https://nuspell.github.io/) tinkantys žodynai.

Šie žodynai naudojami daugumoje atvirojo kodo programų, o „MySpell“ / „Hunspell“ / „Nuspell“ žodynus geba naudoti ir
nemažai nuosavybinės programinės įrangos, kaip antai „Adobe“ produktai bei „macOS“ operacinė sistema.
Kiek išsamesnis tokios PĮ sąrašas – [angliškojoje Vikipedijoje](https://en.wikipedia.org/wiki/Hunspell).

### Parsisiuntimas

Retkarčiais išleidžiamos ir [„GitHub'e“ patalpinamos](https://github.com/ispell-lt/ispell-lt/releases) naujos
„ispell-lt“ versijos. Ten pat galite pasiimti paruoštą naudojimui su „LibreOffice“, „OpenOffice“ ir „Mozillos“
programomis paruoštus „MySpell“ žodyno paketus.

„Debian“ ir „Ubuntu“ pagrindo sistemose šiuos žodynus rasite paketuose `aspell-lt` („Aspell“ tikrintuvui),
`ilithuanian` („ispell“ tikrintuvui), `hunspell-lt` („Hunspell“ ir „Nuspell“ tikrintuvams) ir `hyphen-lt` (lietuviško
skiemenavimo taisyklės). Pastarieji du paketai dabar generuojami iš „LibreOffice“ pirminių tekstų, todėl jų versijų
numeriai kitokie nei pirmųjų dviejų ir nesutampa su „ispell-lt“ projekto versijų numeriais.

### Kontaktai ir įsitraukimas

Žodyno tobulinimui naudojama „GitHub“ platforma. Keisti žodyną repozitorijoje gali
tik [„Ispell-LT“ komandos nariai](https://github.com/ispell-lt), tačiau visi norintys gali siūlyti savo pakeitimus bei
registruoti klaidas, naudodamiesi įprastinėmis „GitHub“ priemonėmis.

Apie rastas klaidas (neteisingą žodžių rašybą, trūkstamus ar neteisingai kaitomus žodžius)
praneškite [užregistruodami klaidą „GitHub'e“](https://github.com/ispell-lt/ispell-lt/issues).

Skiemenavimo taisyklės
----------------------

Greta rašybos tikrinimo žodyno „ispell-lt“ projektas taip pat platina ir lietuviškų skiemenavimo taisyklių failą. 

„Semantika2“
------------

Atskirą „Hunspell“ rašybos tikrintuvui skirtą lietuvišką žodyną parengė projekto „Semantika2“ vykdytojai. Kaip ir
auksčiau minėtasis, šis žodynas turėtų taipogi veikti ir su „MySpell“ bei „Nuspell“ tikrintuvais ir juos naudojančiomis
programomis. Šį žodyną rasite [„GitHub'e“](https://github.com/Semantika2/Hunspell-Zodynai-ir-gramatika-v.45).

Rašybos tikrintuvė internete
----------------------------

Svetainėje [Rasyba.lt](https://rasyba.lietuviuzodynas.lt/) galite greitai patikrinti lietuviško teksto rašybą,
jį tiesiog įklijavę į teksto lauką ir nieko nediegdami į savo kompiuterį.

Automatinio taisymo žodynas
---------------------------

2009–2023 metais veikusioje svetainėje autocorr.akl.lt buvo renkami pasiūlymai automatinio taisymo žodynui (tokio žodyno
porų pavyzdžiai: _gryžti → grįžti_, _akd → kad_), kurį būtų galima naudoti ir platinti su „LibreOffice“, „OpenOffice“
ir kitais programų paketais. Dabar ši svetainė išjungta, tačiau tiek joje surinkti pasiūlymai, tiek jos pačios pirminiai
tekstai patalpinti [„GitHub'e“](https://github.com/rimas-kudelis/autocorr-lt).
