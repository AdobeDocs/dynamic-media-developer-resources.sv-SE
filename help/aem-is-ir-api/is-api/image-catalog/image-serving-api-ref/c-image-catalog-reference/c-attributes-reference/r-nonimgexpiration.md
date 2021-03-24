---
description: Klientcache-TTL för svar som inte är bilder. Anger utgångsintervallet för vissa svar som inte är bilder.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---


# NonImgExpiration{#nonimgexpiration}

Klientcache-TTL för svar som inte är bilder. Anger utgångsintervallet för vissa svar som inte är bilder.

Anger förfallointervallet för vissa svar som inte är bilder, inklusive svar som skickas som svar på följande kommandon:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Egenskaper {#section-d37e3113f4b1468b86b5a14e80d94c83}

Reellt tal, 0 eller högre. Antal timmar till förfallodatum sedan svarsdata genererades. Ange 0 om du alltid vill att svarsbilden ska upphöra att gälla omedelbart, vilket innebär att klientcache-lagring inaktiveras för standardbildsvar. Ange -1 för att markera som *upphör aldrig*.

## Standard {#section-96981360c0234b7f824d2ff7c25a7954}

Ärvs från `default::NonImgExpiration` om det inte är definierat eller om det är tomt.

TTL (Time-To-Live) är längden innan cachen förfaller. Standardvärdet för TTL är 6 minuter.

## Se även {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[katalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribut::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
