---
description: Stöd för hotspot
solution: Experience Manager
title: Stöd för hotspot
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva bilder
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Stöd för hotspot{#hotspot-support}

Visningsprogrammet har stöd för återgivning av hotspot-ikoner ovanpå huvudvyn. Utseendet på hotspot-ikoner styrs via CSS enligt beskrivningen i avsnittet Aktiveringspunkter.

Se [Aktiveringspunkter](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Aktiveringspunkter kan antingen aktivera en snabbvyfunktion på värdwebbsidan genom att aktivera ett JavaScript-återanrop eller dirigera om en användare till en extern webbsida.

## Snabbvyaktiveringspunkter {#section-cda48fc9730142d0bb3326bac7df3271}

Dessa typer av hotspot-områden bör redigeras med åtgärdstypen&quot;snabbvy&quot; i Dynamic Media, AEM Assets - on demand. När en användare aktiverar en sådan hotspot kör visningsprogrammet JavaScript-återanropet `quickViewActivate` och skickar hotspot-data till den. Inbäddningswebbsidan förväntas lyssna efter det här återanropet. När sidan utlöses öppnas en egen snabbvyimplementering.

## Omdirigera till extern webbsida {#section-ef820c71251e4215800bb99c0c9ebe16}

Aktiveringspunkter som skapats för åtgärdstypen&quot;Snabbvy&quot; i Dynamic Media för AEM Assets - dirigerar om användaren till en extern URL. Beroende på inställningarna under utvecklingen öppnas URL-adressen i en ny webbläsarflik, i samma fönster eller i det namngivna webbläsarfönstret.
