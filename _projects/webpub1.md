---
id: collapseOne
title: Osobná webová prezentácia na GitHub pages [Slovak Language]
type: Zadanie 1
date: 2019-06-03
---

## Znenie zadania:

Vytvorte webovú prezentáciu (webové sídlo) o sebe. Zamerajte sa jednak na vaše profesné záujmy (napr. projekty, ktoré riešite/riešili ste, čo vás v informatike najviac baví, fascinuje = váš developerský profil) a jednak vaše osobné záujmy, hobby.

V rámci developerského profilu vytvorte sekciu Webové publikovanie, kde budete publikovať všetky tri vaše vypracované zadania z predmetu.

Využite pritom technológie Git + GitHub Pages + Jekyll + Markdown. Využite potenciál statického generátora Jekyll a jeho templatovacích možností.

Pozor na **plagiarizmus**. Webové sídlo musí byť vaša pôvodná práca, nemôže byť príliš podobné inému existujúcemu sídlu či sídlu vytvorenému pomocou automatického generátora.

Výsledok zadania vložte do AISu do 10. 3. 23:59 ako jeden ZIP archív pomenovaný vaším AIS loginom , ktorý získate ako export projektu z GitHub-u. Okrem toho bude archív obsahovať najviac dva súbory navyše: github.url, kde bude url vášho projektu na GitHub-e, a prípadný readme.txt s pokynmi pre rozbehanie vášho webového sídla (môže obsahovať napr. aj informáciu o podporovanom prehliadači).

## **Dokumentácia:**

### Rozloženie web stránky:

#### Celé sídlo sa skladá z 5 hlavných podstránok (úvodné menu), ktoré obsahujú ešte ďalšie stránky (napr. blog, tag):
 
* **About me** (hlavný index.html v root priečiku) - obsahuje úvodnú stránku so základnými informáciami o mne. Využíva pritom layout default.html, ktorý sa skladá z hlavičky a päty pričom v tele stránky sa nachádza obsah.
* **Skills & education** (priečinok skills_education) - stránka obsahuje prehľad mojich aktuálnych skúseností spolu s dosiahnutým vzdelaním a projektami, na ktorých pracujem. Jej základ tvorí layout default, pričom telo obsahuje layaut projects, ktoré využívam na prezentáciu pri dvoch podstránkach
* **Hobby** (priečinok hobby) - moje osobné záľuby v krátkej prezentácií. Využíva layout default.
* **Blog** (priečinok blog) - osobný blog, ktorý využívam na všeobecnú prezentáciu. Samotná stránka využíva layout default avšak pri konkrétnom poste sa využíva ďalší z layoutov - post, ktorý slúži na zobrazenie konkrétneho článku (názov, autor, a pod.)
	* **Post** - podstránka pre konkrétny blog
	* **Tag** - osobitná stránka na spravovanie generovaných tagov (vytvorené pomocou návodu na stranke: [Long Quian](http://longqian.me/2017/02/09/github-jekyll-tag/). Každý blog obsahuje vlastné tagy, ktoré sa nachádzajú na konci článku, pri generovaní stránky sa všetky tieto tagy vygenerujú a pri kliknutí na tag sa zobrazia blogy, ktoré tento konkrétny tag obsahujú.
* **Web publishing** - osobitná stránka predmetu Webové publikovanie. Základ tvorí layout default pričom (ako pri podstránke **Skills & education**) na prezentáciu projektov využívam layout projects

### Layouty

#### Stránka využíva 4 rôzne layouty:

* **default** - je to základný layout, ktorý dedia všetky podstránky, pričom každá podstránka vypĺňa telo layoutu (buď priamo alebo s pomocou ďalších layoutov)
* **post** - layout pre konkrétny článok (post). S pomocou neho dokážeme zobraziť konkrétne vlastnosti článku (názov, autor, a pod.) spolu s obsahom a tagmi.
* **projects** - layout, ktorý využívam pri osobnej prezentácií, či už skúseností (Skills & education) alebo pri projektoch Webového publikovania (Web publishing).
* **tagpage** - layout, ktorý generuje blogy, obsahujúce konkrétny tag, pričom jednotlivé tagy sa nachádzajú v priečinku *tag* (vytvorené pomocou návodu na stranke: [Long Quian](http://longqian.me/2017/02/09/github-jekyll-tag/), osobitné tagy a premenné som si dopĺňal sám)

### Premenné, kolekcie, filtre, tagy, plugin

#### Stránka spĺňa všetky kvantitatívne požiadavky, pričom v mnohých prípadoch je prvkov oveľa viac. Uvediem aspoň niektoré z nich:

* **premenné** - rôzne premenné obsahujú takmer všetky podstránky (napr. title, date, a pod.), kolekcie (kolekcie projektov, skúseností (skills), blogov (posts)) a premenné využívam aj pri tvorení filtrov (najviac na stránke skills_education - vytváranie polí, spájanie, sort, reverse a pod.)
* **kolekcie** - v projekte sa nachádzajú aktuálne 2 kolekcie (posts a projects), ktoré obsahujú markdown súbory slúžiace ako obsah stránok. Obsahujú mnohé premenné a využívajú sa pri filtorvaní
* **filtre a vlastné tagy** - filtre využívam zväčša pri práci s kolekciami. Napríklad pri prezentácií skúseností. Osobitné tagy využívam napríklad pri layoute default, kde je použitý tag include vo viacerých prípadoch.
	* filtorvanie kolekcie na výber škôl
	* filtrovanie programátorských skúseností pričom sa polia trieda (sort) na základe úrovne skúsenosti a štýl (farba) je podmienený konkrétnym typom skúsenosti (Beginner, Intermediate)
* **plugin** - plugin, ktorý som využil na stránke je prístupný na úvodnej stránke, plugin zabezpečuje pridávanie videí z YouTube

### Štýly a iné

Stránka nevyužíva žiaden vopred pripravený template. Rôzne prvky sú kombináciou bootstrap štýlov, kárt, prezentačných blokov a pod. pričom ich rozloženie som vytváral sám. Osobitné štýly, ktoré som z veľkej časti vytvoril sú prístupné v priečinku *css* (niektoré z nich nie sú čisto mojou prácou - napr. lib a social štýly). Jeden už zo spomínaných prvkov sú špeciálne blogové tagy, ktoré som vytvoril pomocou návodu pričom som implementáciu doplnil o vlastné nové tagy.
