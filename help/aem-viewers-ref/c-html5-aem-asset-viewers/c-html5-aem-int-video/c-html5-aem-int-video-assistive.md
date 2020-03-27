---
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
seo-description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
seo-title: Teknikstöd
solution: Experience Manager
title: Teknikstöd
topic: Dynamic media
uuid: 0abed8d4-9754-47b1-9de7-cce665de03b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har roll `region` och `aria-label` attribut inställt som standard på visningsprogrammets namn. Du kan styra etiketten med `Container.LABEL` lokaliseringssymbolen.

Knappar har rollen `button` och beskrivande text med `aria-label` attribut. Värdet för `aria-label` attributet fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad ställs attributet in i enlighet med detta `aria-disabled` .

Slider-komponenter har rollen `slider` med attribut `aria-valuenow`, `aria-valuemin`och `aria-valuemax` för att beskriva den aktuella skjutreglagepositionen.

Miniatyrbilder har rollen `dialog` med `aria-label` attribut som styrs av `ThumbnailGridView.LABEL` lokaliseringssymbolen. Enskilda miniatyrbilder har en roll `button`. Om en miniatyrbild är markerad får den `aria-selected` attributet angivet till `true`.

Komponenter som visar färgrutor har rollen `listbox` med `aria-label` attributet inställt på värdet för den komponentens `LABEL` lokaliseringssymbol. Enskilda färgrutor har rollen `option` med `aria-setsize` och `aria-posinset` attribut som beskriver färgrutans placering i uppsättningen. Om du väljer en färgruta får den attributuppsättningen `aria-selected` som `true`.

Nedrullningsbara listor aktiveras av knappar med ytterligare `aria-haspopup` attribut inställda på `true` och `aria-controls` attribut som refererar till det faktiska nedrullningsbara panelelementet. Själva listrutan har rollen `menu` med underelement `menuitem`. Varje menyalternativ har det angivna `aria-label` -attributet.

Modala dialogrutor har rollen `dialog`. Dialogrutans rubrikelement refereras av `aria-labelledby` -attributet.
