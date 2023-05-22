---
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
solution: Experience Manager
title: Teknikstöd
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har en roll `region` och `aria-label` som standard anges visningsprogrammets namn. Du kan styra etiketten med `Container.LABEL` lokaliseringssymbol.

Knappar har rollen `button` och beskrivande text med `aria-label` -attribut. Värdet för `aria-label` -attributet fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad visas `aria-disabled` -attributet anges därefter.

Huvudvyn har en roll `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av `ROLE_DESCRIPTION` lokaliseringssymbol för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, kommer texten för användartipset från `USAGE_HINT` lokaliseringssymbol. Om en resurs har en etikett definierad i fältet UserData, `aria-label` -attributet anges med värdet för den etiketten.

Aktiveringspunkter, regioner och bildscheman har rollen `button` och beskrivande text med `aria-label` -attribut, med värdet för aktiveringspunkten eller bildschemaetiketten. När användaren fokuserar på aktiveringspunkter eller bildscheman visas navigeringstips för tangentbordsanvändare med `aria-describedby`, med texten för användartipset som kommer från `USAGE_HINT` lokaliseringssymbol.

Miniatyrbilder har rollen `dialog` med `aria-label` attribut som styrs av `ThumbnailGridView.LABEL` lokaliseringssymbol. Enskilda miniatyrbilder har en roll `button`. Om en miniatyrbild är markerad visas den `aria-selected` attribut inställt på `true`.

Komponenter som visar färgrutor har rollen `listbox` med `aria-label` attributet inställt på värdet för `LABEL` lokaliseringssymbol för den komponenten. Enskilda färgrutor har rollen `option` med `aria-setsize` och `aria-posinset` attribut som beskriver färgrutans placering i uppsättningen. Om en färgruta är markerad hämtas `aria-selected` attribut inställt på `true`.

Listrutor aktiveras av knappar med ytterligare `aria-haspopup` attribut inställt på `true` och `aria-controls` attribut som refererar till det faktiska nedrullningsbara panelelementet. Den nedrullningsbara panelen har rollen `menu` med underelement som har rollen `menuitem`. Varje menyalternativ har `aria-label` angivet attribut.

Sökgränssnittet är grupperat i elementet med rollen `search`. Indatafältet för sökning har rollen `searchbox` och refererar till den informativa etikett som styrs av `SearchPanel.INFO_PROMPT` lokaliseringssymbol med `aria-describedby` -attribut.

Modala dialogrutor har rollen `dialog`. Dialogrutans rubrikelement refereras av `aria-labelledby` -attribut.
