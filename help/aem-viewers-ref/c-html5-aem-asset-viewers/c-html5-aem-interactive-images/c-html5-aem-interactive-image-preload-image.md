---
title: Förhandsladda bild
description: Förhandsladda bilder är en statisk förhandsvisningsbild som läses in direkt efter att init()-metoden har anropats och visas medan Viewer SDK-bibliotek, resurser och förinställningsinformation hämtas. Syftet med förinläsningsbilden är att visuellt förbättra läsarens inläsningstid och snabbt visa innehållet för användaren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Förhandsladda bild{#preload-image}

Förhandsladda bilder är en statisk förhandsvisningsbild som läses in direkt efter att init()-metoden har anropats och visas medan Viewer SDK-bibliotek, resurser och förinställningsinformation hämtas. Syftet med förinläsningsbilden är att visuellt förbättra läsarens inläsningstid och snabbt visa innehållet för användaren.

Förhandsladda bilder fungerar bra för den vanligaste inbäddningsmetoden för visningsprogram, som är responsiv inbäddning med obegränsad höjd. Se rubriken [Responsiv designinbäddning med obegränsad höjd](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Funktionen har dock vissa begränsningar när andra inbäddningsmetoder eller särskilda konfigurationsalternativ används. Förhandsladda bilder kan inte återges korrekt i följande fall:

* När visningsprogrammet är fast i storlek och storleken definieras antingen med konfigurationsattributet `stagesize` i visningsprogrammets förinställningspost. Du kan också använda CSS-filen för det externa visningsprogrammet för visningsprogrammets behållarelement på den översta nivån.
* När du använder den flexibla storleksinbäddningen med den bredd- och höjddefinierade metoden för visningsprograminbäddning. Se rubriken [Bädda in flexibel storlek med bredd och höjd definierad](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Inaktivera funktionen för förhandsladda bilder med konfigurationsattributet `preloadImage` om du använder visningsprogrammet i något av de åtgärdslägen som anges ovan.

Dessutom används inte förinläsningsbilden - även om den är aktiverad i konfigurationen - om visningsprogrammet är inbäddat i DOM-elementet är dolt med CSS-inställningen `display:none` eller om det är frånkopplat från DOM-trädet.
