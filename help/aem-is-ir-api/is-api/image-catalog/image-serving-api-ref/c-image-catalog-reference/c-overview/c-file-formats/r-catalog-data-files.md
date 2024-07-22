---
description: Katalogdatafiler kan ha vilket namn och filsuffix som helst (förutom .ini). De kan enkelt underhållas med program som stöder tabbavgränsade textdatafiler som Microsoft Excel och Access.
solution: Experience Manager
title: Katalogdatafiler
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Katalogdatafiler{#catalog-data-files}

Katalogdatafiler kan ha vilket namn och filsuffix som helst (förutom .ini). De kan enkelt underhållas med program som stöder tabbavgränsade textdatafiler som Microsoft Excel och Access.

En katalogdatafil är i princip en tvådimensionell tabell och består av en rubrikpost som identifierar datakolumner och ett valfritt antal dataposter (rader). Fält i både rubrik- och dataposter avgränsas med `<TAB>` tecken. Posterna avgränsas med en enda `<CR>` (ASCII-kod `0xD`), en enda `<LF>` (ASCII-kod `0xA`) eller ett `<CR><LF>`-par.

Rubrikposten måste innehålla de exakta namnen för varje datafält. Tomma fält tillåts inte i rubrikraden. Datafältnamn är inte skiftlägeskänsliga. Alla fältnamn måste vara unika.

Det går inte att använda blankstegstecken som fältavgränsare. Inga mellanslag tillåts i rubrikposten. I dataposter räknas alla blanksteg i början eller slutet av ett datafält som en del av det datafältet.

I dataposterna anger två intilliggande `<TAB>` tecken ett tomt fält. Tomma fält kan ärva standardvärden från antingen katalogattributen eller från serverns standardvärden.

Datafält kan även omslutas av citattecken. De får inte innehålla `<CR>`, `<LF>` eller `<TAB>` tecken, såvida inte datavärdet är av typen text och omsluts av citattecken. Datafälten får inte vara HTTP-kodade.

Flera datavärden i samma fält avgränsas med kommatecken, om inget annat anges.

Kolumner vars namn börjar med &quot;.&quot; ignoreras. Detta gör det möjligt att lagra data i bildkataloger, vilket inte är av intresse för Image Serving. Kolumner med okända rubriknamn ignoreras och en varning skrivs till loggfilen.

Fältnamn kan bestå av en valfri kombination av ASCII-bokstäver, siffror samt &quot;-&quot; och &quot;_&quot;.

En eller flera kolumner kan användas som indexnycklar. Om samma tangent förekommer mer än en gång i samma datafil gäller den senare instansen.
