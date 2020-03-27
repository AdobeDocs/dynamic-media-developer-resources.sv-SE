---
description: 'null'
seo-description: 'null'
seo-title: Stöd för hotspot- och bildscheman
solution: Experience Manager
title: Stöd för hotspot- och bildscheman
topic: Dynamic media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Stöd för hotspot- och bildscheman{#hotspot-and-image-maps-support}

Visningsprogrammet har stöd för återgivning av hotspot-ikoner och bildschemaområden ovanpå huvudvyn. Utseendet på hotspot-ikoner och -regioner styrs via CSS enligt beskrivningen i avsnittet Anpassa hotspot-områden och bildscheman.

Se [Aktiveringspunkter och bildscheman](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Aktiveringspunkter och regioner kan antingen aktivera en snabbvyfunktion på värdwebbsidan genom att aktivera ett JavaScript-återanrop eller dirigera om en användare till en extern webbsida.

## Snabbvyaktiveringspunkter {#section-cda48fc9730142d0bb3326bac7df3271}

Dessa typer av hotspot-områden eller bildscheman bör redigeras med åtgärdstypen&quot;Snabbvy&quot; i Dynamic Media, från AEM. När en användare aktiverar ett sådant hotspot- eller bildschema kör visningsprogrammet `quickViewActivate` JavaScript-återanropet och skickar hotspot- eller bildschemats data till det. Inbäddningswebbsidan förväntas lyssna efter det här återanropet. När sidan utlöses öppnas en egen snabbvyimplementering.

## Omdirigera till extern webbsida {#section-ef820c71251e4215800bb99c0c9ebe16}

Aktiveringspunkter eller bildscheman som skapats för åtgärdstypen&quot;Snabbvy&quot; i dynamiska media i AEM dirigerar om användaren till en extern URL. Beroende på inställningarna under utvecklingen öppnas URL-adressen i en ny webbläsarflik, i samma fönster eller i det namngivna webbläsarfönstret.
