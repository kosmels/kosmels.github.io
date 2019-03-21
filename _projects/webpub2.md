---
id: collapseTwo
title: Transformácia vybraného dokumentu do formátu DocBook [Slovak Language]
type: Zadanie 2
date: 2019-03-20
---

## Znenie zadania:

Predmetom 2. zadania je spracovanie vybraného dokumentu (ideálne bakalárskeho projektu) z pôvodného ľubovoľného (Word, OpenOffice, LaTeX, …) formátu do formátu DocBook a vygenerovanie cieľového tvaru v PDF. Výsledný dokument bude mať rozsah minimálne 10 a maximálne 15 strán. Do rozsahu sa nezapočítavajú úvodné strany (obsah, zoznamy obrázkov a tabuliek), použitá literatúra a prílohy.

Požadované a kontrolné konštrukcie sú:

* štandardné členenie textu na kapitola, podkapitola, podpodkapitola, príloha, generovaný obsah,
* zvýraznenie slov, zvýraznenie členenia textu odrážkami alebo číslovaním,
* odkazy na iné časti vlastného dokumentu, prípadne odkazy na URL,
* poznámka pod čiarou,
* zoznam použitej literatúry a zdrojov vrátane ich citácie v texte,
* vloženie obrázku a tabuliek, odkazy na ne v texte; zoznam obrázkov a tabuliek v úvode alebo závere textu,
* vytvorenie registra pojmov (indexu) s pojmami hierarchicky usporiadanými do dvoch úrovni, napríklad „cykly, while“, „cykly, for“ (najmenej ako ukážku na 10-15 pojmoch na predvedenie práce s registrom).

Súčasťou požiadaviek na zadanie je vytvorenie správy o zadaní 2, ktorá bude súčasťou vašej stránky o Webovom publikovaní na GitHube. Správa o rozsahu 150-250 slov bude obsahovať informácie o použitých elementoch a atribútoch, prípadne ukážky XML/XSLT demonštrujúce vykonané prispôsobenie DocBook šablon (nepovinné).

Na transformáciu zo zdrojového formátu DocBook do PDF použite upravenú šablónu na základe šablóny od Jiřího Koska (obsahuje i ukážku).

Výsledok 2. zadania vložte do **24. 03. 23:59** do AISu ako jeden ZIP archív pomenovaný vaším AIS loginom (Z2-aislogin.zip). Archív musí obsahovať:

* zdrojové texty vo formáte DocBook a ďalšie súbory súvisiace s obsahom (napr. obrázky),
* skripty potrebné na preklad (dávkové súbory .bat)
* cieľový tvar súborov a pôvodný tvar textu bakalárskeho projektu (ideálne PDF),
* sprievodný textový súbor
* archív obsahovať najviac dva súbory navyše: github.url, s url vášho projektu na GitHub-e

Archív **nesmie** obsahovať žiadne externé knižnice (saxon, …).

### Dokumentácia:

Dokument je členený na dve hlavné kapitoly, ktoré obsahujú rôzny počet podkapitol a podpodkapitol. Príloha na konci dokumentu obsahuje správu k priebežnej práci na bakalárskej práci. Generovaný obsah sme rozšírili v súbore *thesis.xsl* o zoznam obrázkov a tabuliek (konkrétne v riadku 176 sme pridali parametre *figure a table*). Na rôznych miestach v dokumente sa nachádzajú zvýraznené slová (kurzíva alebo bold). V podkapitole 2.10. Regularization sa nachádza príklad neusporiadaného zoznamu. Dokument obsahuje taktiež aj konkrétne citácie (tag <\\blockqoute>).

Ďalšie príklady:

* Odkazy a URL - v texte sa na rôznych miestach odkazujem na iné kapitoly alebo časti dokumentu (hlavne na úvodných stranách - kapitola 2.1.). Odkazy na stránky sa nachádzajú v bibliografických záznamoch na konci dokumentu.
* Poznámky pod čiarou - napríklad strany 15, 17
* Bibliografia a odkazy - dokument obsahuje 3 bibliografické záznamy na ktoré sa odkazujem v rôznych častiach dokumentu
* Práca s obrázkami a tabuľkami - dokument obsahuje 2 obrázky (s. 12, 14), ktoré sú referencované v kapitolach v ktorých sa aj nachádzajú. Tabuľku obsahuje kapitola 2.12. a rovnako obsahuje aj jej referenciu
* Register pojomv - register sa nachádza na predposlednej strane dokumentu, obsahuje rôzne pojmy alebo slovné spojenie v rôznych úrovniach (najhlbšia úroveň je 3)

Ďalšie úpravy:

Úpravy sme vykonali aj priamo v šablónach (súbory s príponou .xsl). Konkrétne sme upravili velkosť okrajov (na 1.2in), pridali generovanie zoznamu obrázkov a tabuliek a odstránili obrázok z titulnej strany.