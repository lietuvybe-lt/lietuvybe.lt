---
title: Daugiskaitos formos
type: page
aliases:
    - /lokalizuotojams/gramatines-formos/
menu:
    main:
        weight: 30
        parent: Lokalizuotojams
---

Lietuvių kalboje naudojamos trys skaitos formos (vienaskaita ir du daugiskaitos variantai). Kadangi tokie vertimai kaip „21 failai“ niekam nepatinka, o mūsų kalba šiuo požiūriu visai nėra unikali, kai kurios vertimo technologijos suteikia galimybę naudoti daugiau kaip dvi skaitos formas.

„gettext“ (`*.po` failai)
-------------------------

Jeigu lokalizuodami „gettext“ naudojančią programą pasitelkiate specialiai lokalizavimui skirtą įrankį ir joje nurodote, jog verčiate į lietuvių kalbą, tuomet labai tikėtina, jog jums papildomai nieko daryti nereikia – jūsų įrankis turėtų pats aptikti eilutes, kurias verčiant, galima naudoti skaitos formas, ir tokių eilučių atveju jums pateiks tris atskirus laukus išverstam tekstui įvesti.

Jeigu vertimui naudojate paprastą teksto redaktorių, lietuviško „gettext“ vertimo failo antraštėje nurodykite tokią skaitos formų eilutę:

```shell
"Plural-Forms: nplurals=3; plural=(n%10==1 && n%100!=11 ? 0 : n%10>=2 && (n%100<10 || n%100>=20) ? 1 : 2);\n"
```

Tai atlikus, failo antraštė turi atrodyti maždaug taip:

```shell {hl_lines=12}
msgid ""
msgstr ""
"Project-Id-Version: Programos pavadinimas ir versija\n"
"Report-Msgid-Bugs-To: \n"
"POT-Creation-Date: 2004-03-06 20:36+0200\n"
"PO-Revision-Date: 2004-03-07 11:50+0200\n"
"Last-Translator: Vardenis Pavardenis <vardenis@pvz.lt>\n"
"Language-Team: Lithuanian <komp_lt@konferencijos.lt>\n"
"MIME-Version: 1.0\n"
"Content-Type: text/plain; charset=UTF-8\n"
"Content-Transfer-Encoding: 8bit\n"
"Plural-Forms: nplurals=3; plural=(n%10==1 && n%100!=11 ? 0 : n%10>=2 && (n%100<10 || n%100>=20) ? 1 : 2);\n"
```

Dabar, versdami ištekliaus eilutes su nurodytu `msgid_plural` parametru, ją verskite į visus tris daugiskaitos variantus. Pavyzdys:

```shell {hl_lines=4}
#: src/window.c:942
#, c-format
msgid "%d file (%s)"
msgid_plural "%d files (%s)"
msgstr[0] "%d failas (%s)"   # 1 failas (failo vardas)
msgstr[1] "%d failai (%s)"   # 2-9 failai (failų vardai)
msgstr[2] "%d failų (%s)"    # 10 failų (failų vardai)
```

„Qt“ pagrindu veikiančios programos (`*.ts`, `*.qm` failai)
-----------------------------------------------------------
[„Qt“][Qt] yra komercinių bibliotekų, platinamų taipogi ir atviruoju kodu, rinkinys.
Šių bibliotekų pagrindu veikia [„KDE“][KDE] grafinė aplinka „UNIX“ genties operacinėms sistemoms ir daugybė kitų tiek atvirųjų, tiek komercinių programų.

Kaip ir „gettext“ atveju, „Qt“ vertimuose yra galimybė naudoti kelias skaitos formas.
Pačių formų kiekio ir pasirinkimo būdo nereikia aprašinėti kiekviename vertimo faile atskirai – tai padaryta [centralizuotai][Qt numerus].
Lietuvių kalba čia taip pat aprašyta su trimis formomis, iš kurių naudotina forma išrenkama pagal tą patį algoritmą, kaip ir „gettext“. Lietuviško `*.ts` vertimo failo ištrauka, kurioje naudojama ši galimybė, atrodo štai taip:

```xml {hl_lines=1}
<message numerus="yes">
    <source>%n file(s)</source>
    <comment>number of chosen files</comment>
    <translation>
        <numerusform>%n failas</numerusform>
        <numerusform>%n failai</numerusform>
        <numerusform>%n failų</numerusform>
    </translation>
</message>
```

[KDE]: https://www.kde.org
[Qt]: https://www.qt.io
[Qt numerus]: https://github.com/qt/qt/blob/0a2f2382541424726168804be2c90b91381608c6/tools/linguist/shared/numerus.cpp#L340-L341