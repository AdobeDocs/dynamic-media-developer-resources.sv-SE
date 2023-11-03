---
title: Katalogdatafiler
description: Katalogdatafiler kan ha vilket namn och filsuffix som helst (förutom .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Katalogdatafiler{#catalog-data-files}

Katalogdatafiler kan ha vilket namn och filsuffix som helst (förutom `.ini`).

Katalogdatafiler kan enkelt underhållas med program som stöder tabbavgränsade textdatafiler som Microsoft® Excel och Access.

En katalogdatafil är i princip en tvådimensionell tabell och består av en rubrikpost som identifierar datakolumner och ett valfritt antal dataposter (rader). Fält i både rubrik- och dataposter avgränsas med en `<TAB>` tecken. Posterna avgränsas av en enda `<CR>` (ASCII-kod `0xD`), en `<LF>` (ASCII-kod `0xA`), eller en `<CR><LF>` par.

Rubrikposten måste innehålla de exakta namnen för varje datafält. Tomma fält tillåts inte i rubrikraden. Datafältnamn är inte skiftlägeskänsliga. Alla fältnamn måste vara unika.

Inget annat tomt utrymme än `<TAB>` fältavgränsare tillåts i rubrik- och dataposter.

I dataposterna finns två intilliggande `<TAB>` tecken anger ett tomt fält. Tomma fält ärver standardvärden från antingen katalogattributen eller från serverns standardvärden.

Datafälten får inte innehålla `<CR>`, `<LF>`, eller `<TAB>` om inte datavärdet är av typen text och omsluts av enkla eller dubbla citattecken. Koda inte HTTP-datafält.

Flera datavärden i samma fält avgränsas med kommatecken (&#39;,&#39;), om inget annat anges.

Kolumner vars namn börjar med &#39;.&#39; ignoreras; detta tillåter lagring av data i materialkataloger som inte är av intresse för bildåtergivning. Kolumner med okända rubriknamn ignoreras och en varning skrivs till loggfilen.

Fältnamn kan bestå av vilken kombination som helst av ASCII-bokstäver, siffror och&quot;-&quot; och&quot;_&quot;.

En eller flera kolumner kan användas som indexnycklar. Om samma tangent förekommer mer än en gång i samma datafil gäller den senare instansen.
