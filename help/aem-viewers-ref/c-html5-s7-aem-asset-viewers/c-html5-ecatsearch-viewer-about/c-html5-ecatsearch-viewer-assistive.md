---
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
solution: Experience Manager
title: Teknikstöd
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning,Tillgänglighet
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har rollattributen `region` och `aria-label` inställda som standard på visningsprogrammets namn. Du kan styra etiketten med lokaliseringssymbolen `Container.LABEL`.

Knappar har rollen `button` och beskrivande text med attributet `aria-label`. Värdet för attributet `aria-label` fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad ställs attributet `aria-disabled` in därefter.

Huvudvyn har rollen `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av lokaliseringssymbolen `ROLE_DESCRIPTION` för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, texten för användartipset kommer från lokaliseringssymbolen `USAGE_HINT`. Om en resurs har en etikett definierad i fältet UserData ställs attributet `aria-label` in med värdet för den etiketten.

Aktiveringspunkter, regioner och bildscheman har rollen `button` och en beskrivande textuppsättning med attributet `aria-label`, med värdet för aktiveringspunkten eller bildschemats etikett. När användaren fokuserar på aktiveringspunkter eller bildscheman visas navigeringstips för tangentbordsanvändare med `aria-describedby`, där texten för användartipset kommer från lokaliseringssymbolen `USAGE_HINT`.

Miniatyrbilder har rollen `dialog` med attributet `aria-label` som styrs av språksymbolen `ThumbnailGridView.LABEL`. Enskilda miniatyrbilder har rollen `button`. Om du väljer en miniatyrbild får den `aria-selected`-attributet `true`.

Komponenter som visar färgrutor har rollen `listbox` med attributet `aria-label` inställt på värdet för `LABEL`-lokaliseringssymbolen för den komponenten. Enskilda färgrutor har rollen `option` med attributen `aria-setsize` och `aria-posinset` som beskriver färgrutans position i uppsättningen. Om du väljer en färgruta får den attributet `aria-selected` inställt på `true`.

Listrutor aktiveras av knappar med ytterligare `aria-haspopup`-attribut inställt på `true` och `aria-controls`-attributet som refererar till det faktiska nedrullningsbara panelelementet. Den nedrullningsbara panelen har rollen `menu` med underelement som har rollen `menuitem`. Varje menyalternativ har det angivna `aria-label`-attributet.

Användargränssnittet för sökning är grupperat i elementet med rollen `search`. Indatafältet för sökning har rollen `searchbox` och refererar till den informativa etikett som styrs av `SearchPanel.INFO_PROMPT`-lokaliseringssymbolen med attributet `aria-describedby`.

Modala dialogrutor har rollen `dialog`. Dialogrutans rubrikelement refereras av attributet `aria-labelledby`.
