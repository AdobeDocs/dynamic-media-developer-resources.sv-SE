---
description: Förhandsladda bilder är en statisk förhandsvisningsbild som läses in direkt efter att init()-metoden har anropats och visas medan Viewer SDK-bibliotek, resurs- och förinställningsinformation hämtas. Syftet med förinläsningsbilden är att visuellt förbättra läsarens inläsningstid och snabbt visa innehållet för användaren.
solution: Experience Manager
title: Förhandsladda bild
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Förhandsladda bild{#preload-image}

Förhandsladda bilder är en statisk förhandsvisningsbild som läses in direkt efter att init()-metoden har anropats och visas medan Viewer SDK-bibliotek, resurs- och förinställningsinformation hämtas. Syftet med förinläsningsbilden är att visuellt förbättra läsarens inläsningstid och snabbt visa innehållet för användaren.

Förhandsladda bilder fungerar bra för den vanligaste inbäddningsmetoden för visningsprogram, som är responsiv inbäddning med obegränsad höjd. Se rubriken [Responsiv designinbäddning med obegränsad höjd](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

Funktionen har dock vissa begränsningar när andra inbäddningsmetoder eller särskilda konfigurationsalternativ används. Förhandsladda bilder kan inte återges korrekt i följande fall:

* När visningsprogrammet har en fast storlek och storleken definieras antingen med konfigurationsattributet `stagesize` i visningsprogrammets förinställningspost eller i den externa visningsprogrammets CSS-fil för visningsprogrammets behållarelement på den översta nivån.
* När den flexibla storleksinbäddningen med den bredd- och höjddefinierade metoden för visningsprograminbäddning används. Se rubriken [Bädda in flexibel storlek med bredd och höjd definierad](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Du kan behöva inaktivera funktionen för förhandsladda bilder med konfigurationsattributet `preloadImage` om du använder visningsprogrammet i något av de åtgärdslägen som anges ovan.

Dessutom används inte förinläsningsbilden - även om den är aktiverad i konfigurationen - om visningsprogrammet är inbäddat i DOM-elementet är dolt med CSS-inställningen `display:none` eller om det är frånkopplat från DOM-trädet.
