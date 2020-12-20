---
description: Katalogdatafiler kan ha vilket namn och filsuffix som helst (förutom .ini). De kan enkelt underhållas med program som stöder tabbavgränsade textdatafiler som Microsoft Excel och Access.
seo-description: Katalogdatafiler kan ha vilket namn och filsuffix som helst (förutom .ini). De kan enkelt underhållas med program som stöder tabbavgränsade textdatafiler som Microsoft Excel och Access.
seo-title: Katalogdatafiler
solution: Experience Manager
title: Katalogdatafiler
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f66e2fe-5b8a-43d3-bf2e-8dd79da6a581
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---


# Katalogdatafiler{#catalog-data-files}

Katalogdatafiler kan ha vilket namn och filsuffix som helst (förutom .ini). De kan enkelt underhållas med program som stöder tabbavgränsade textdatafiler som Microsoft Excel och Access.

En katalogdatafil är i princip en tvådimensionell tabell och består av en rubrikpost som identifierar datakolumner och ett valfritt antal dataposter (rader). Fält i både huvud- och dataposter avgränsas med enkla `<TAB>`-tecken. Posterna avgränsas med en enda `<CR>` (ASCII-kod `0xD`), en enda `<LF>` (ASCII-kod `0xA`) eller ett `<CR><LF>`-par.

Rubrikposten måste innehålla de exakta namnen för varje datafält. Tomma fält tillåts inte i rubrikraden. Datafältnamn är inte skiftlägeskänsliga. Alla fältnamn måste vara unika.

Det går inte att använda blankstegstecken som fältavgränsare. Inga mellanslag tillåts i rubrikposten. I dataposter räknas alla blanksteg i början eller slutet av ett datafält som en del av datafältet.

I dataposterna anger två intilliggande `<TAB>`-tecken ett tomt fält. Tomma fält kan ärva standardvärden från antingen katalogattributen eller från serverns standardvärden.

Datafält kan även omslutas av citattecken. De får inte innehålla `<CR>`, `<LF>` eller `<TAB>` tecken, såvida inte datavärdet är av typen text och omsluts av citattecken. Datafälten får inte vara HTTP-kodade.

Flera datavärden i samma fält avgränsas med kommatecken, om inget annat anges.

Kolumner vars namn börjar med &quot;.&quot; ignoreras. Detta gör det möjligt att lagra data i bildkataloger, vilket inte är av intresse för Image Serving. Kolumner med okända rubriknamn ignoreras och en varning skrivs till loggfilen.

Fältnamn kan bestå av en valfri kombination av ASCII-bokstäver, siffror samt &quot;-&quot; och &quot;_&quot;.

En eller flera kolumner kan användas som indexnycklar. Om samma tangent förekommer mer än en gång i samma datafil gäller den senare instansen.
