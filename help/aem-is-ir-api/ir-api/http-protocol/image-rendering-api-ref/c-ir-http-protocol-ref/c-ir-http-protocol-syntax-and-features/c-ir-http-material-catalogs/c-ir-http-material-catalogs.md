---
description: Materialkataloger har flera funktioner.
seo-description: Materialkataloger har flera funktioner.
seo-title: Materialkataloger *
solution: Experience Manager
title: Materialkataloger *
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Materialkataloger *{#material-catalogs}

Materialkataloger har flera funktioner.

* Tillåt beständig definition av material, inklusive alla materialegenskaper.

   Material som definieras i materialkatalogen kan refereras med ett enkelt ID i stället för en uppsättning materialegenskaper.
* Ange standardvärden för vissa begärandeattribut, t.ex. JPEG-kvalitet eller en standardstorlek för svarsbilder.
* Hantera vinjetter, ICC-profiler och förfrågningsmallar.

Även om inga särskilda materialkataloger har definierats är alla funktioner i materialkataloger tillgängliga via standardkatalogen ( [!DNL default.ini]).

Återgivningsmaterial kan anges uttryckligen i förfrågningar med hjälp av materialattribut, men i många fall är det mer önskvärt att dölja detaljerna för materialet från webbplatsen med hjälp av materialkataloger. src=-kommandon accepterar katalogreferenser i stället för explicita filsökvägar. En katalogpost består av ` [ *[!DNL catId]*/] *[!DNL itemId]*`, där ` *[!DNL catId]*` identifierar en materialkatalog och ` *[!DNL itemId]*` identifierar en post i katalogen. Om ` *[!DNL catId]*` inte anges används sessionskatalogen (se nedan).

En katalogpost matchas korrekt om (a) ` *[!DNL catId]*` matchar `attribute::RootId`-värdet för en materialkatalog och (b) ` *[!DNL recId]*` matchar värdet för katalogen::Id i samma katalog. Om matchningen lyckas ställs materialets attribut (inklusive `src=`) in på data från katalogposten. Om MSS innehåller ytterligare attribut för det här materialet förutom src=, åsidosätter de värdena från katalogposten.

Om ` *[!DNL recId]*` inte kan matchas mot en katalogpost ersätts ` *[!DNL catId]*` med `attribute::RootPath` från katalogen och den resulterande sökvägen antas sedan vara en enkel filsökväg. Andra standardattribut (t.ex. `attribute::Resolution`) kan också ärvas från materialkatalogen.

Vinjetter och ICC-profiler kan specificeras i materialkataloger som liknar materialets i sig och angivna egenskaper. Dessutom innehåller vinjetteringskartan också mallbehållaren.

**Se även**

Referens för materialkatalog, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
