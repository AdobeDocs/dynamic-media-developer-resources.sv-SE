---
title: Stöd för hotspot- och bildscheman
description: Stöd för hotspot- och bildscheman
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 8d5dbc2d2b5e228f8496fd71633bf1cb96218226
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Stöd för hotspot- och bildscheman{#hotspot-and-image-maps-support}

Visningsprogrammet har stöd för återgivning av hotspot-ikoner och bildschemaområden ovanpå huvudvyn. Utseendet på hotspot-ikoner och -regioner styrs via CSS enligt beskrivningen i avsnittet Anpassa hotspot-områden och bildscheman.

Se [Aktiveringspunkter och bildscheman](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Aktiveringspunkter och regioner kan antingen aktivera en snabbvyfunktion på värdwebbsidan genom att utlösa ett JavaScript-återanrop eller dirigera om en användare till en extern webbsida.

## Snabbvisa hotspot-områden {#section-cda48fc9730142d0bb3326bac7df3271}

Den här typen av hotspot-områden eller bildscheman bör redigeras med åtgärdstypen&quot;Quickview&quot; i Dynamic Media, Adobe Experience Manager. När en användare aktiverar ett sådant hotspot- eller bildschema kör visningsprogrammet JavaScript-återanropet `quickViewActivate` och skickar hotspot- eller bildschemats data till det. Inbäddningswebbsidan förväntas lyssna efter det här återanropet. När sidan utlöses öppnas en egen QuickView-implementering.

## Omdirigera till extern webbsida {#section-ef820c71251e4215800bb99c0c9ebe16}

Aktiveringspunkter eller bildscheman som skapats för åtgärdstypen&quot;Quickview&quot; i Dynamic Media i Experience Manager dirigerar om användaren till en extern URL. Beroende på inställningarna under utvecklingen öppnas URL-adressen i en ny webbläsarflik, i samma fönster eller i det namngivna webbläsarfönstret.
