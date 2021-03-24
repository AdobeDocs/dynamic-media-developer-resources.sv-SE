---
description: Felsvarsbild. Bildredigering returnerar vanligtvis en felstatus med ett textmeddelande när ett fel inträffar.
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---


# ErrorImage{#errorimage}

Felsvarsbild. Bildredigering returnerar vanligtvis en felstatus med ett textmeddelande när ett fel inträffar.

`attribute::ErrorImage` gör att en bild, katalogpost eller mall kan returneras vid fel.

>[!NOTE]
>
>Saknade bilder kan också hanteras med `attribute::DefaultImage`.

En Image Serving-mall kan konfigureras, vilket kan återge felmeddelandetexten i svarsbilden. Följande fördefinierade variabler kan inkluderas i `$error.title`-mallen, som ersätts med en kort felbeskrivning, och `$error.message`, som ersätts med en mer detaljerad felbeskrivning (detaljnivån konfigureras med `attribute::ErrorDetail`).

HTTP-status 200 returneras om felbilden/mallen kan bearbetas. Om ett fel inträffar under bearbetningen returneras HTTP-felstatusen och ett textmeddelande.

## Egenskaper {#section-f460c6c2dd1f46b29f9a79b093575f45}

Textsträng. Om det anges måste det vara en giltig katalog::Id-värde i en bildkatalog eller en relativ (till `attribute::RootPath`) eller absolut sökväg till en bildfil som är tillgänglig för Image Server.

## Standard {#section-2885f289e5714ddca665a6aee401967f}

Ärvs från `default::ErrorImage` om inte definierat. Om den är definierad men tom inaktiveras felbildens beteende, även om `default::ErrorImage` är definierat och HTTP-felstatusen och textmeddelandet returneras.

## Exempel {#section-c92090abe1d247529542a8dd4960c2e6}

För att få svarsbilder med felmeddelandet återgivet till bilden måste vi först definiera mallen i bildkatalogen. I det här fallet skapar vi en post i vår bildkatalog med namnet `onError`, som innehåller följande i `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

Mallen är registrerad med `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

I det här exemplet återges texten med standardteckensnitt, standardfärg och standardteckenstorlek.

## Se även {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
