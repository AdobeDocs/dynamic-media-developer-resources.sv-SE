---
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
seo-description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
seo-title: Teknikstöd
solution: Experience Manager
title: Teknikstöd
topic: Dynamic media
uuid: 8565383e-5c13-4af0-9b6e-2d583c18f19c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har roll `region` och `aria-label` attribut inställt som standard på visningsprogrammets namn. Du kan styra etiketten med `Container.LABEL` lokaliseringssymbolen.

Knappar har rollen `button` och beskrivande text angiven med `aria-label` -attributet. Värdet för `aria-label` attributet fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad ställs attributet in i enlighet med detta `aria-disabled` .

Huvudvyn har en roll `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av `ROLE_DESCRIPTION` lokaliseringssymbolen för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, texten för användartipset kommer från `USAGE_HINT` lokaliseringssymbolen. Om en resurs har en etikett definierad i fältet UserData, ställs attributet in med värdet för den etiketten. `aria-label`

Aktiveringspunkter, regioner och bildscheman har rollen `button` och beskrivande text med `aria-label` attribut, med värdet för aktiveringspunkten eller bildschemats etikett. När användaren fokuserar på aktiveringspunkter eller bildscheman visas navigeringstips för tangentbordsanvändare med `aria-describedby`, där texten för användartipset kommer från `USAGE_HINT` lokaliseringssymbolen.

Miniatyrbilder har rollen `dialog` med `aria-label` attribut som styrs av `ThumbnailGridView.LABEL` lokaliseringssymbolen. Enskilda miniatyrbilder har en roll `button`. Om en miniatyrbild är markerad får den `aria-selected` attributet angivet till `true`.

Komponenter som visar färgrutor har rollen `listbox` med `aria-label` attributet inställt på värdet för den komponentens `LABEL` lokaliseringssymbol. Enskilda färgrutor har rollen `option` med `aria-setsize` och `aria-posinset` attribut som beskriver färgrutans placering i uppsättningen. Om du väljer en färgruta får den attributuppsättningen `aria-selected` som `true`.

Listrutor aktiveras av knappar med ytterligare `aria-haspopup` attribut inställt på `true` `aria-controls` och det attribut som refererar till det faktiska nedrullningsbara panelelementet. Själva listrutan har rollen `menu` med underelement `menuitem`. Varje menyalternativ har det angivna `aria-label` -attributet.

Modala dialogrutor har rollen `dialog`. Dialogrutans rubrikelement refereras av `aria-labelledby` -attributet.
