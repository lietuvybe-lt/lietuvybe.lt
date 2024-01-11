---
title: Rašybos tikrinimo priemonės
linkTitle: Rašybos tikrinimas
type: page
lastmod: 2023-12-14
aliases:
    - /naudotojams/rasybos-tikrinimas/
menu:
    main:
        weight: 10
        parent: Naudotojams
---

Rašybos tikrinimo žodynas „ispell-lt“
-------------------------------------

„ispell-lt“ yra lietuvių kalbos rašybos tikrinimo taisyklės ir žodynas standartiniam UNIX rašybos tikrinimo
įrankiui [„Ispell“](http://fmg-www.cs.ucla.edu/geoff/ispell.html). Iš tų pačių pradinių duomenų „ispell-lt“ projekte
generuojami
ir [„Aspell“](http://aspell.net/), [„MySpell“](http://code.google.com/a/apache-extras.org/p/ooo-myspell/), [„Hunspell“](http://hunspell.sourceforge.net/)
ir [„Nuspell“](https://nuspell.github.io/) tinkantys žodynai.

Šie žodynai naudojami daugumoje atvirojo kodo programų, o „MySpell“/„Hunspell“/„Nuspell“ žodynus geba naudoti ir nemažai
nuosavybinių programų, kaip antai „Adobe“ produktai bei „macOS“ operacinė sistema.

### Parsisiuntimas

Karts nuo karto išleidžiamos ir[„GitHub'e“ patalpinamos](https://github.com/ispell-lt/ispell-lt/releases) naujos
„ispell-lt“ versijos. Ten pat galite pasiimti paruoštą vartojimui su „OpenOffice“ arba „Mozillos“ programomis paruoštus
„MySpell“ žodyno paketus.

„Debian“ paketus sukūrė Kęstutis Biliūnas, o dabar juos prižiūri „Debian“ komanda. Jų sąrašas:

* aspell-lt – žodynas „Aspell“ tikrintuvui
* ilithuanian – žodynas „ispell“ tikrintuvui
* myspell-lt – žodynas „MySpell“ ir „Hunspell“ tikrintuvams
* openoffice.org-hyphenation-lt – skiemenavimo taisyklės

Naujesnėse „Debian“ laidose pastarieji du paketai pakeisti generuojamais iš „LibreOffice“ saugyklų:

* hunspell-lt – žodynas „MySpell“ ir „Hunspell“ tikrintuvams
* hyphen-lt – skiemenavimo taisyklės

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

Atskirą „Hunspell“ žodyną parengė projekto „Semantika2“ vykdytojai. Šį žodyną taip pat galima
rasti [„GitHub'e“](https://github.com/Semantika2/Hunspell-Zodynai-ir-gramatika-v.45).

Automatinio taisymo žodynas
---------------------------

Nuo 2009 m. pabaigos veikusioje svetainėje autocorr.akl.lt su lankytojų pagalba buvo renkami pasiūlymai automatinio
taisymo žodynui (tokio žodyno porų pavyzdžiai: gryžti → grįžti, akd → kad), kurį būtų galima naudoti ir platinti su
„LibreOffice“, „OpenOffice“ ir kitais programų paketais. 2023 m. pabaigoje ši svetainė išjungta, tačiau tiek joje
surinkti pasiūlymai, tiek jos pačios pirminiai tekstai
patalpinti [„GitHub'e“](https://github.com/rimas-kudelis/autocorr-lt).
