---
id: collapseTwo
title: XML prezentácia [Slovak Language]
type: Zadanie 3
date: 2019-04-25
---

## Znenie zadania:

Analyzujte možnosti zápisu jednoduchej prezentácie v jazyku XML. Identifikujte základné súčasti prezentácie a navrhnite XML elementy pre ich označkovanie (metadátové, štrukturálne, inline). Dbajte na znovupoužiteľnosť a vyvarujte sa redundancií. Návrh elementov zrealizujte opísaním typu dokumentu pomocou vybraného jazyka (DTD, XSD, RELAX NG) spolu s vysvetlením účelu jednotlivých elementov. Vo vami navhrnutom jazyku vytvorte ukážkovú prezentáciu, ktorá bude demonštrovať možnosti tvorby prezentácií podľa definície typu dokumentu.

Navrhnite a vytvorte XSLT šablóny pre konverziu prezentácie z XML do XHTML+CSS a pre konverziu prezentácie z XML do PDF. Klaďte dôraz na znovupoužitie jednotlivých šablon pre viaceré výstupné formáty. Umožnite zadávanie parametrov transformácií.

Súčasťou požiadaviek na zadanie je vytvorenie správy o zadaní 3, v ktorej zdokumentujete splenie jednotlivých bodov zadania. Správa bude súčasťou vašej stránky o Webovom publikovaní na GitHube.

**Hodnotenie (max 14 bodov):**

* opis typu dokumentu + opis účelu navrhnutých elementov - možnosť výberu (práve jedného) z variantov: DTD, XML Schema alebo RELAX NG
* vytvorenie ukážkovej XML prezentácie demonštrujúcej možnosti definície typu dokumentu (max 2 body)
* základný návrh XSL transformácií, ich vhodnosť, parametrizácia (max 3 body)
* vytvorenie XSLT pre konverziu prezentácie z XML -> XHTML+CSS (max 3 body) (každý slide bude v samostatnom XHTML súbore)
* vytvorenie XSLT pre konverziu prezentácie XML -> PDF (max 2 body)

Výsledok zadania vložte do **28. 4. 23:59** do AISu ako jeden ZIP archív pomenovaný vaším AIS loginom (Z3-aislogin.zip). Archív **musí** obsahovať:

* zdrojové súbory a ďalšie súbory súvisiace s obsahom (napr. obrázky),
* skripty potrebné na preklad (dávkové súbory .bat),
* cieľový tvar súborov,
* sprievodný textový súbor, ktorý obsahuje zoznam súborov obsiahnutých v archíve a spôsob prekladu (transformáciu) do cieľového formátu.

Archív **nesmie** obsahovať žiadne externé knižnice (saxon, …).

### Dokumentácia:

Vytvorili sme jednoduchú prezentáciu v jazyku HTML, ktorá reprezentuje našu bakalársku prácu. Základ tvorí súbor *zadanie3.xml*, ktorý obsahuje dáta k požadovanej prezentácií. Súbory *zadanie3.xsl* a *pdf_xs.xsl* obsahujú XSLT šablóny na transformáciu XML dokumentu do HTML a PDF. Koreňový element (*presentation*) obsahuje 4 slajdy, ktoré neskôr spracujeme do výsledných prezentácií. 

Opis plnenia požiadaviek:

* Opis typu dokumentu - na kontrolu dokumentu XML sme využili DTD pravidlá
* Vytvorili sme XML dokument, ktorý sme následne overili pomocou DTD
* XSL transformácie sú reprezentované v dokumentoch *zadanie3.xsl* (slúži na konverziu XML do webovej prezentácie XHTML+CSS) a *pdf_xs.xsl* (slúži na konverziu XML dokumentu do PDF verzie prezentácie)
* v oboch prípadoch (HTML aj PDF) sa generujú jednotlivé slajdy na osobitné stránky (vygenerované .html dokumenty alebo jeden PDF dokument)

Opis dokumentov:

Štruktúra XML dokumentu pozostáva z koreňového elementu *presentation*, ktorý obsahuje aktuálne 4 elementy reprezentujúce slajdy (*slide* element). Každý z týchto elementov má vlastný nadpis, ktorý je povinným elementom a rôzne elementy, ktoré obsahujú jednotlivé slajdy.

XSLT dokument pre konverziu XML do XHTML obsahuje základné šablóny pre jednotlivé slajdy spolu s CSS štýlmi. XSLT dokument na PDF konverziu obsahuje podobne ako predchádzajúci dokument základné šablóny, ktoré sú spracované pomocou XSL FO (Formating objects) elementov.