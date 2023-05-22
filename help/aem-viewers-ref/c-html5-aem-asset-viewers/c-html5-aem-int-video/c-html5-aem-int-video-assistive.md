---
title: Teknikstöd
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har en roll `region` och `aria-label` som standard anges visningsprogrammets namn. Du kan styra etiketten med `Container.LABEL` lokaliseringssymbol.

Knappar har rollen `button` och beskrivande text med `aria-label` -attribut. Värdet för `aria-label` -attributet fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad `aria-disabled` -attributet anges därefter.

Slider-komponenter har rollen `slider` med attribut `aria-valuenow`, `aria-valuemin`och `aria-valuemax` för att beskriva den aktuella skjutreglagepositionen.

Miniatyrbilder har rollen `dialog` med `aria-label` attribut som styrs av `ThumbnailGridView.LABEL` lokaliseringssymbol. Enskilda miniatyrbilder har en roll `button`. Om en miniatyrbild är markerad visas den `aria-selected` attribut inställt på `true`.

Komponenter som visar färgrutor har rollen `listbox` med `aria-label` attributet inställt på värdet för `LABEL` lokaliseringssymbol för den komponenten. Enskilda färgrutor har rollen `option` med `aria-setsize` och `aria-posinset` attribut som beskriver färgrutans placering i uppsättningen. Om en färgruta är markerad hämtas `aria-selected` attribut inställt på `true`.

Listrutor aktiveras av knappar med ytterligare `aria-haspopup` attribut inställt på `true` och `aria-controls` attribut som refererar till det faktiska nedrullningsbara panelelementet. Den nedrullningsbara panelen har rollen `menu` med delelement som har rollen `menuitem`. Varje menyalternativ har `aria-label` angivet attribut.

Modala dialogrutor har rollen `dialog`. Dialogrutans rubrikelement refereras av `aria-labelledby` -attribut.
