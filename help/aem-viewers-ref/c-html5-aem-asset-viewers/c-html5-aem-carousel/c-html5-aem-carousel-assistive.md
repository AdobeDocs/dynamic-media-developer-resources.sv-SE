---
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
seo-description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
seo-title: Teknikstöd
solution: Experience Manager
title: Teknikstöd
topic: Dynamic media
uuid: 72b414f4-b647-4afa-a409-a8ba90227d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har roll `region` och `aria-label` attribut inställt som standard på visningsprogrammets namn. Du kan styra etiketten med `Container.LABEL` lokaliseringssymbolen.

Knappar har rollen `button` och beskrivande text med `aria-label` attribut. Värdet för `aria-label` attributet fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad ställs attributet in i enlighet med detta `aria-disabled` .

Knappar som gör att du kan navigera i karusellbilder har etiketter som uppdateras under körning beroende på vilken bildruta som är vald. Mallen för knappens etikett anges med `CAROUSELVIEWER_TOOLTIP_GOTO` lokaliseringssymbol.

Huvudvyn har en roll `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av `ROLE_DESCRIPTION` lokaliseringssymbolen för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, texten för användartipset kommer från `USAGE_HINT` lokaliseringssymbolen. Om en resurs har en etikett definierad i fältet UserData, ställs attributet in med värdet för den etiketten. `aria-label`

Aktiveringspunkter, regioner och bildscheman har rollen `button` och beskrivande text med `aria-label` attribut, med värdet för aktiveringspunkten eller bildschemats etikett. När användaren fokuserar på aktiveringspunkter eller bildscheman visas navigeringstips för tangentbordsanvändare med `aria-describedby`, där texten för användartipset kommer från `USAGE_HINT` lokaliseringssymbolen.
