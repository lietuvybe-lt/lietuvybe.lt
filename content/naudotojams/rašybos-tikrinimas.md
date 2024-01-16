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

„ispell-lt“ yra lietuvių kalbos rašybos tikrinimo taisyklės ir žodynas įprastiniam UNIX rašybos tikrinimo
įrankiui [„Ispell“](http://fmg-www.cs.ucla.edu/geoff/ispell.html). Iš tų pačių pradinių duomenų „ispell-lt“ projekte generuojami
ir [„Aspell“](http://aspell.net/), [„MySpell“](http://code.google.com/a/apache-extras.org/p/ooo-myspell/),
[„Hunspell“](http://hunspell.sourceforge.net/) bei [„Nuspell“](https://nuspell.github.io/) tinkantys žodynai.

Šie žodynai naudojami daugumoje atvirojo kodo programų, o „MySpell“ / „Hunspell“ / „Nuspell“ žodynus geba naudoti ir
nemažai nuosavybinės programinės įrangos, kaip antai „Adobe“ produktai bei „macOS“ operacinė sistema.
Kiek išsamesnis tokios PĮ sąrašas – [angliškojoje Vikipedijoje](https://en.wikipedia.org/wiki/Hunspell).

### Parsisiuntimas

Retkarčiais išleidžiamos ir [„GitHub'e“ patalpinamos](https://github.com/ispell-lt/ispell-lt/releases) naujos
„ispell-lt“ versijos. Ten pat galite pasiimti paruoštą vartojimui su „OpenOffice“ arba „Mozillos“ programomis paruoštus
„MySpell“ žodyno paketus.

„Debian“ ir „Ubuntu“ pagrindo sistemose šiuos žodynus rasite šiuose paketuose:

* `aspell-lt` – žodynas „Aspell“ tikrintuvui
* `ilithuanian` – žodynas „ispell“ tikrintuvui
* `hunspell-lt` – žodynas „MySpell“, „Hunspell“ ir „Nuspell“ tikrintuvams
* `hyphen-lt` – skiemenavimo taisyklės

Pastarieji du paketai dabar generuojami iš „LibreOffice“ šaltinių, todėl jų versijų numeriai visiškai kitokie nei
pirmųjų dviejų.

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

Automatinio taisymo žodynas
---------------------------

Nuo 2009 m. pabaigos veikusioje svetainėje autocorr.akl.lt su lankytojų pagalba buvo renkami pasiūlymai automatinio
taisymo žodynui (tokio žodyno porų pavyzdžiai: _gryžti → grįžti_, _akd → kad_), kurį būtų galima naudoti ir platinti su
„LibreOffice“, „OpenOffice“ ir kitais programų paketais. 2023 m. pabaigoje ši svetainė išjungta, tačiau tiek joje
surinkti pasiūlymai, tiek jos pačios pirminiai tekstai
patalpinti [„GitHub'e“](https://github.com/rimas-kudelis/autocorr-lt).
