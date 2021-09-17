---
title: Teknikstöd
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har rollattributen `region` och `aria-label` inställda som standard på visningsprogrammets namn. Du kan styra etiketten med lokaliseringssymbolen `Container.LABEL`.

Knappar har rollen `button` och beskrivande textuppsättning med attributet `aria-label`. Värdet för attributet `aria-label` fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad ställs `aria-disabled`-attributet in därefter.

Knappar som gör att du kan navigera i karusellbilder har etiketter som uppdateras under körning beroende på vilken bildruta som är vald. Mallen för den här knappetiketten är inställd med en `CAROUSELVIEWER_TOOLTIP_GOTO`-lokaliseringssymbol.

Huvudvyn har rollen `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av lokaliseringssymbolen `ROLE_DESCRIPTION` för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, texten för användartipset kommer från lokaliseringssymbolen `USAGE_HINT`. Om en resurs har en etikett definierad i fältet UserData ställs attributet `aria-label` in med värdet för den etiketten.

Aktiveringspunkter, regioner och bildscheman har rollen `button` och en beskrivande textuppsättning med attributet `aria-label`, med värdet för aktiveringspunkten eller bildschemats etikett. När användaren fokuserar på aktiveringspunkter eller bildscheman visas navigeringstips för tangentbordsanvändare med `aria-describedby`, där texten för användartipset kommer från lokaliseringssymbolen `USAGE_HINT`.
