---
title: Materialkataloger
description: Materialkataloger har flera funktioner.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Materialkataloger {#material-catalogs}

Materialkataloger har flera funktioner.

* Tillåt beständig definition av material, inklusive alla materialegenskaper.

  Material som definieras i materialkatalogen kan refereras med ett enkelt ID i stället för en uppsättning materialegenskaper.
* Ange standardvärden för vissa begärandeattribut, t.ex. JPEG-kvalitet eller en standardstorlek för svarsbilder.
* Hantera vinjetter, ICC-profiler och förfrågningsmallar.

Även om inga särskilda materialkataloger är definierade är alla funktioner i materialkataloger tillgängliga som standardkatalog ( [!DNL default.ini]).

Återgivningsmaterial kan anges uttryckligen i förfrågningar med hjälp av materialattribut, men det är ofta mer önskvärt att dölja detaljerna om material från webbplatsen med hjälp av materialkataloger. src=-kommandon accepterar katalogreferenser i stället för explicita filsökvägar. En katalogpost består av ` [ *[!DNL catId]*/] *[!DNL itemId]*`, där ` *[!DNL catId]*` identifierar en materialkatalog och ` *[!DNL itemId]*` identifierar en post i katalogen. If ` *[!DNL catId]*` har inte angetts används sessionskatalogen (se nedan).

En katalogpost matchas korrekt om (a) ` *[!DNL catId]*` matchar `attribute::RootId` värdet av en materialkatalog och b) ` *[!DNL recId]*` matchar värdet för katalogen::Id i samma katalog. Om det finns en lyckad matchning är materialets attribut (inklusive `src=`) ställs in på data från katalogposten. Om MSS innehåller ytterligare attribut för det här materialet förutom src=, åsidosätter de värdena från katalogposten.

If ` *[!DNL recId]*` kan inte matchas mot en katalogpost. ` *[!DNL catId]*` ersätts med `attribute::RootPath` från katalogen och den slutliga sökvägen antas sedan vara en enkel filsökväg. Andra standardattribut (till exempel `attribute::Resolution`) kan också ärvas från materialkatalogen.

Vinjetter och ICC-profiler kan specificeras i materialkataloger som liknar materialets i sig och angivna egenskaper. Dessutom innehåller vinjetteringskartan också mallbehållaren.

**Se även**

Referens för materialkatalog. [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
