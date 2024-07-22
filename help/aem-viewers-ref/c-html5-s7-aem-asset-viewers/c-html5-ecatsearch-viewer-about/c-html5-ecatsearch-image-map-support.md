---
description: Visningsprogrammet för eCatalog-sökning stöder återgivning av bildschemaikoner ovanför huvudvyn.
solution: Experience Manager
title: Stöd för bildscheman
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Stöd för bildscheman{#image-map-support}

Visningsprogrammet för eCatalog-sökning stöder återgivning av bildschemaikoner ovanför huvudvyn.

Utseendet på mappningsikoner styrs via CSS enligt beskrivningen i [Bildschemaeffekt](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Bildscheman utför någon av följande tre åtgärder: omdirigering till en extern webbsida, popup-aktivering av panelen Info samt interna hyperlänkar.

## Omdirigera till en extern webbsida {#section-32ebe3c3a7f74892a428c5d48801de4d}

Bildschemats `href`-attribut har en URL till den externa resursen, antingen explicit specificerad eller inkapslad i någon av de JavaScript-mallfunktioner som stöds: `loadProduct()`, `loadProductCW()` och `loadProductPW()`.

Följande är ett exempel på en enkel URL-omdirigering:

`href=http://www.adobe.com`

I det här exemplet är samma URL omsluten med funktionen `loadProduct()`:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Tänk på att när du lägger till JavaScript-koden i attributet `HREF` för din bildschema körs koden på klientens dator. Kontrollera därför att JavaScript-koden är säker.

## Aktivering av popup-meny i panelen Info {#section-7aa036420af646d1ad8cdc388add0b57}

Om du vill arbeta med Info-panelerna har ett bildschema attributet `ROLLOVER_KEY`. Ange också attributet `href` samtidigt, annars stör den externa URL-bearbetningen popup-aktiveringen i panelen Info.

Kontrollera slutligen att visningsprogramkonfigurationen innehåller rätt värden för parametrarna `InfoPanelPopup.template` och `InfoPanelPopup.infoServerUrl` (om så önskas).

>[!NOTE]
>
>Tänk på att när du konfigurerar popup-rutan för panelen Info körs den HTML-kod och JavaScript-kod som skickas till panelen Info på klientens dator. Se därför till att sådan HTML-kod och JavaScript-kod är säkra.

## Interna hyperlänkar {#section-6afa4fb2fe564c429e0201f019a95849}

När du klickar på ett bildschema sker en intern sidväxling inuti visningsprogrammet. Om du vill använda den funktionen har ett `href`-attribut i bildschemat följande specialformat:

` href=target: *`idx`*`

där `*`idx`*` är ett nollbaserat index för kataloguppslaget.

Följande är ett exempel på ett `href`-attribut för ett bildschema som pekar på 3D-uppslaget i eCatalog:

`href=target:2`
