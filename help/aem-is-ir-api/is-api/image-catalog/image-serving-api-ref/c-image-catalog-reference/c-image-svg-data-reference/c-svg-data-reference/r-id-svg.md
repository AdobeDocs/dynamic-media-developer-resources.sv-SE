---
description: ID
solution: Experience Manager
title: ID
uuid: a700472c-e1eb-4eb0-95ff-7afd4ce27931
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# ID{#id}

Vanligtvis en kort och unik identifierare, t.ex. ett SKU-nummer, kanske med någon typ av suffix, t.ex. om en SKU har flera bilder eller har språkspecifika variationer. Kan också vara en mer komplex sträng som ser mer ut som en filsökväg, med stöd för enkel anpassning av webbplatser med Image Serving.

>[!NOTE]
>
>Bilden och SVG-tabellerna sammanfogas till en enda tabell när bildkatalogen läses in. Id-värden måste vara unika för båda tabellerna. SVG-posten ignoreras om bildtabellen innehåller en post med samma ID-värde. Statiskt innehåll hanteras med en separat tabell. Statiska innehållsobjekt och bild-/SVG-objekt kan därför ha samma ID-värden.

## Egenskaper {#section-874a6853f67b4b229341ca76682884ae}

Textsträng. Obligatoriskt. Postidentifierare för bildens/SVG-datatabellen eller den statiska innehållsdatatabellen. Varje `catalog::Id`-värde i den här bildkatalogen/SVG-katalogen eller i den här statiska innehållskatalogen måste vara unikt och får inte innehålla tecknen &#39;,&#39;.

## Standard {#section-a26e7d83a5ee44b5918baef82ee48e14}

Ingen.

## Se även {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
