---
description: Statiskt innehållstypfilter. Anger en filtersträng för statiskt innehåll som levereras via /is/content.
seo-description: Statiskt innehållstypfilter. Anger en filtersträng för statiskt innehåll som levereras via /is/content.
seo-title: type
solution: Experience Manager
title: type
topic: Scene7 Image Serving - Image Rendering API
uuid: 44906190-516c-481c-9714-bb19d77af33c
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# type{#type}

Statiskt innehållstypfilter. Anger en filtersträng för statiskt innehåll som levereras via /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Textfiltersträng. </p></td> 
 </tr> 
</table>

Servern jämför val med värdet `catalog::Type` för det begärda statiska innehållsobjektet. Objektet returneras till klienten om värdena matchar (skiftlägeskänsliga), annars returneras ett fel.

## Egenskaper {#section-529b088434a44a9f86a64ef548d2925b}

Stöds endast för begäranden om statiskt innehåll (inte bilder) som hanteras via. Ignoreras om `catalog::Type` är tom eller inte definierad.

## Standard {#section-e9e8f51d0a01452183ccb510efd87d46}

Ingen typmatchning används om `type=` inte har angetts eller är tom.

## Se även {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Serverar statiskt innehåll](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da) (inte bildinnehåll),  [katalog::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
