---
title: Lietuvybė tinklalapių adresuose
type: page
menu:
    main:
        weight: 90
        parent: Naudotojams
---

Turbūt jau niekam nebekyla klausimų, ar lietuviškus rašmenis galima naudoti tinklalapiuose.
Tačiau ar galima juos naudoti svetainių ir tinklalapių adresuose?

Atsakymas į šį klausimą labai paprastas – taip!

Nuo 2004 metų Lietuvoje galima registruoti sričių vardus su visomis lietuvių kalbos abėcėlės raidėmis, įskaitant devynias savitąsias.
Tokie sričių vardai registruojami, naudojant specialų jų kodavimo būdą, leidžiantį išlaikyti suderinamumą su senomis sistemomis, vadinamą [„Punycode“][Punycode].
Sričių vardus su visomis lietuviškomis (ir ne tik!) raidėmis palaiko visos interneto naršyklės, tačiau [saugumo sumetimais][IDN homograph attack] tokius vardus adreso lauke jos rodo ne visada.

Su savitosiomis lietuviškomis raidėmis tinklalapių adresų dalyje, kuri nėra srities vardas (po pirmojo pavienio pasvirojo brūkšnio) situacija panaši: nors „po kapotu“ savitosios lietuviškos raidės adresuose yra koduojamos, kad „sutilptų“ į ASCII kodų lentelę, visos šiuolaikinės naršyklės, naudotojui adreso laukelyje įvedus adresą su savitosiomis lietuviškomis raidėmis ar kitais ženklais, tokį adresą perkoduos [reikiamu būdu][IRI].
Tiesa, jei tinklalapio adresas su savitosiomis lietuviškomis raidėmis bus įrašytas kaip saito adresas kitame tinklalapyje, nenaudojančiame UTF-8 koduotės, toks saitas gali neveikti.
Tokiu atveju derėtų pakoreguoti patį saitą, į jį įrašant tinkamai perkoduotą tinklalapio adresą.
Visgi, šiais laikais ši problema vargu ar bėra aktuali, nes kone visi bent jau nauji tinklalapiai šiais laikais yra koduojami būtent UTF-8 koduote.
Be to, jei tinklalapį redaguojate „ką matai, tą ir gauni“ tipo priemonėmis, tikėtina, kad adresą, jei reikia, už jus užkoduos jos.

Atkreipkite dėmesį, jog svetainės ar tinklalapio adresas su savitosiomis lietuviškomis raidėmis ir be jų nurodo į potencialiai skirtingus išteklius.
Pavyzdžiui, į naršyklės adreso lauką įvedus adresą lietuvyb**e**.lt, jus pasitiks kitas tinklalapis, nei įvedus adresą lietuvyb**ė**.lt.
Naršydami nepamirškite šio niuanso, kad neatsidurtumėte apgavikų pinklėse.
O jei registruoti srities vardą ir kurti svetainę dar tik ketinate patys – apsvarstykite galimybę įsigyti tiek vardą su savitosiomis lietuviškomis raidėmis, jei tokių yra jūsų norimame žodyje, tiek be jų.
Įsigydami abu adresus ir vieną iš jų automatiškai nukreipdami į antrąjį, padėsite savo lankytojams nepasiklysti.

Beje, pastebėkite, jog ši svetainė naudoja savitąsias lietuviškas raides tiek srities varde (lietuvyb**ė**.lt), tiek tinklalapių adresuose.

Yra dar vienas nedidelis nesklandumas: kai kurios naršyklės, kopijuojant adresą su savitosiomis lietuviškomis raidėmis, jį automatiškai užkoduoja, tokiu būdu paversdamos žymiai sunkiau skaitomu.
Tai daroma atgalinio suderinamumo tikslais, tačiau šiais laikais vargu ar praktiška, ypač kai norima adresą palikti matomą (pavyzdžiui, spaudinyje).
Yra pora gan paprastų būdų šį nesklandumą apeiti.
Pirmasis – prieš kopijuojant adresą, jį pakoreguoti taip, kad naršyklė jo nelaikytų adresu.
Pavyzdžiui, į adreso pradžią įterpiant kokį nors papildomą ženklą, kad ir tarpą. Kopijuoti galima su tuo ženklu arba be jo (tada to ženklo nereikės iš kopijos pašalinti).
Kitas būdas – pažymėti ir kopijuoti tik dalį adreso, pavyzdžiui, vietoj _https&colon;//lietuvybė.lt_ tik _lietuvybė.lt_.

Plačiau apie lietuviškus tinklalapių vardus skaitykite dr. Gintauto Grigo 2021 metų straipsnyje [„Gražūs internetiniai vardai. Kaip išsaugoti jų grožį?“][Gintauto straipsnis] „Lietuvos aido“ svetainėje.

[Punycode]: https://en.wikipedia.org/wiki/Punycode "Punycode – Wikipedia – en.wikipedia.org"
[IDN homograph attack]: https://en.wikipedia.org/wiki/IDN_homograph_attack "IDN homograph attack – Wikipedia – en.wikipedia.org"
[IRI]: https://en.wikipedia.org/wiki/Internationalized_Resource_Identifier "Internationalized Resource Identifier – Wikipedia – en.wikipedia.org"
[Gintauto straipsnis]: https://www.aidas.lt/lt/visuomene/article/25345-04-11-grazus-internetiniai-vardai-kaip-issaugoti-ju-grozi "04.11. Gražūs internetiniai vardai. Kaip išsaugoti jų grožį? – Lietuvos aidas – aidas.lt"
