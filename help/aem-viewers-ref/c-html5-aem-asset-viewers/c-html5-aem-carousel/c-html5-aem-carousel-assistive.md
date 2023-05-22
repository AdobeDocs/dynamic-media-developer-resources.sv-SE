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

Visningsprogramelementet på den översta nivån har en roll `region` och `aria-label` som standard anges visningsprogrammets namn. Du kan styra etiketten med `Container.LABEL` lokaliseringssymbol.

Knappar har rollen `button` och beskrivande text med `aria-label` -attribut. Värdet för `aria-label` -attributet fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad `aria-disabled` -attributet anges därefter.

Knappar som gör att du kan navigera i karusellbilder har etiketter som uppdateras under körning beroende på vilken bildruta som är vald. Mallen för knappetiketten är inställd med `CAROUSELVIEWER_TOOLTIP_GOTO` lokaliseringssymbol.

Huvudvyn har en roll `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av `ROLE_DESCRIPTION` lokaliseringssymbol för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, kommer texten för användartipset från `USAGE_HINT` lokaliseringssymbol. Om en resurs har en etikett definierad i fältet UserData, `aria-label` -attributet anges med värdet för den etiketten.

Aktiveringspunkter, regioner och bildscheman har rollen `button` och beskrivande text med `aria-label` -attribut, med värdet för aktiveringspunkten eller bildschemaetiketten. När användaren fokuserar på aktiveringspunkter eller bildscheman visas navigeringstips för tangentbordsanvändare med `aria-describedby`, med texten för användartipset som kommer från `USAGE_HINT` lokaliseringssymbol.
