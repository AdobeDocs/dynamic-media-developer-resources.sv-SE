---
description: Visningsprogrammet för eCatalog-sökning stöder återgivning av bildschemaikoner ovanför huvudvyn.
seo-description: Visningsprogrammet för eCatalog-sökning stöder återgivning av bildschemaikoner ovanför huvudvyn.
seo-title: Stöd för bildscheman
solution: Experience Manager
title: Stöd för bildscheman
topic: Dynamic media
uuid: 22ba8168-b384-4eda-a147-ce8172cfed11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Stöd för bildscheman{#image-map-support}

Visningsprogrammet för eCatalog-sökning stöder återgivning av bildschemaikoner ovanför huvudvyn.

Utseendet på mappningsikoner styrs via CSS enligt beskrivningen i [Bildschemaeffekt](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Bildscheman utför någon av följande tre åtgärder: omdirigera till en extern webbsida, popup-aktivering av panelen Info och interna hyperlänkar.

## Omdirigera till en extern webbsida {#section-32ebe3c3a7f74892a428c5d48801de4d}

Bildschemats attribut har en URL till den externa resursen, antingen explicit specificerad eller inkapslad i en av JavaScript-mallfunktionerna som stöds: `href` `loadProduct()`, `loadProductCW()`och `loadProductPW()`.

Följande är ett exempel på en enkel URL-omdirigering:

`href=http://www.adobe.com`

I det här exemplet är samma URL omsluten med `loadProduct()` funktionen:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Tänk på att koden körs på klientens dator när du lägger till JavaScript-koden i attributet för `HREF` bildschemat. Kontrollera därför att JavaScript-koden är säker.

## Aktivering av popup-meny i panelen Info {#section-7aa036420af646d1ad8cdc388add0b57}

Om du vill arbeta med panelen Info har ett bildschema `ROLLOVER_KEY` attributuppsättningen. Du kan också ställa in attributet samtidigt, annars stör den externa URL-bearbetningen popup-aktiveringen i panelen Info. `href`

Kontrollera slutligen att visningsprogrammets konfiguration innehåller rätt värden för `InfoPanelPopup.template` och eventuellt `InfoPanelPopup.infoServerUrl` parametrar.

>[!NOTE]
>
>Tänk på att när du konfigurerar Info Panel-popup körs den HTML-kod och JavaScript-kod som skickas till Info-panelen på klientens dator. Kontrollera därför att sådan HTML-kod och JavaScript-kod är säkra.

## Interna hyperlänkar {#section-6afa4fb2fe564c429e0201f019a95849}

När du klickar på ett bildschema sker en intern sidväxling inuti visningsprogrammet. Om du vill använda den funktionen har ett attribut i bildschemat följande specialformat: `href`

` href=target: *`idx`*`

där ` *`idx`*` är ett nollbaserat index för kataloguppslaget.

Nedan följer ett exempel på ett attribut för ett bildschema som pekar på 3D-uppslaget i eCatalog: `href`

`href=target:2`
