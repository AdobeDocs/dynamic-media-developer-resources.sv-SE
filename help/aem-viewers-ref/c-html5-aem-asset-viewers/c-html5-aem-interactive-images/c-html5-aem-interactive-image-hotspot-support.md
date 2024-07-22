---
title: Stöd för hotspot
description: Stöd för hotspot
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Stöd för hotspot{#hotspot-support}

Visningsprogrammet har stöd för återgivning av hotspot-ikoner ovanpå huvudvyn. Utseendet på hotspot-ikoner styrs via CSS enligt beskrivningen i avsnittet Aktiveringspunkter.

Se [Aktiveringspunkter](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Aktiveringspunkter kan antingen aktivera en snabbvyfunktion på värdwebbsidan genom att aktivera ett JavaScript-återanrop eller dirigera om en användare till en extern webbsida.

## Snabbvisa hotspot-områden {#section-cda48fc9730142d0bb3326bac7df3271}

Dessa typer av hotspot-områden bör redigeras med åtgärdstypen&quot;QuickView&quot; i Dynamic Media, Adobe Experience Manager Assets - On-demand. När en användare aktiverar en sådan hotspot kör visningsprogrammet JavaScript-återanropet `quickViewActivate` och skickar hotspot-data till det. Inbäddningswebbsidan förväntas lyssna efter det här återanropet. När sidan utlöses öppnas en egen QuickView-implementering.

## Omdirigera till extern webbsida {#section-ef820c71251e4215800bb99c0c9ebe16}

Aktiveringspunkter som skapats för åtgärdstypen&quot;Snabbvy&quot; i Dynamic Media för Experience Manager Assets - Används vid behov omdirigeras användaren till en extern URL. Beroende på inställningarna under utvecklingen öppnas URL-adressen i en ny webbläsarflik, i samma fönster eller i det namngivna webbläsarfönstret.
