---
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
solution: Experience Manager
title: Teknikstöd
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp,Tillgänglighet
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# Stöd för hjälpfunktioner{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har rollattributen `region` och `aria-label` inställda som standard på visningsprogrammets namn. Du kan styra etiketten med lokaliseringssymbolen `Container.LABEL`.

Knappar har rollen `button` och beskrivande textuppsättning med attributet `aria-label`. Värdet för attributet `aria-label` fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad ställs `aria-disabled`-attributet in därefter.

Slider-komponenter har rollen `slider` med attributen `aria-valuenow`, `aria-valuemin` och `aria-valuemax` som beskriver den aktuella skjutreglagepositionen.

Miniatyrbilder har rollen `dialog` med attributet `aria-label` som styrs av språksymbolen `ThumbnailGridView.LABEL`. Enskilda miniatyrbilder har rollen `button`. Om du väljer en miniatyrbild får den `aria-selected`-attributet `true`.

Komponenter som visar färgrutor har rollen `listbox` med attributet `aria-label` inställt på värdet för `LABEL`-lokaliseringssymbolen för den komponenten. Enskilda färgrutor har rollen `option` med attributen `aria-setsize` och `aria-posinset` som beskriver färgrutans position i uppsättningen. Om du väljer en färgruta får den attributet `aria-selected` inställt på `true`.

Nedrullningsbara listor aktiveras av knappar med ytterligare `aria-haspopup`-attribut inställt på `true` och `aria-controls`-attribut som refererar till det faktiska nedrullningsbara panelelementet. Den nedrullningsbara panelen har rollen `menu` med underelement som har rollen `menuitem`. Varje menyalternativ har det angivna `aria-label`-attributet.

Modala dialogrutor har rollen `dialog`. Dialogrutans rubrikelement refereras av attributet `aria-labelledby`.
