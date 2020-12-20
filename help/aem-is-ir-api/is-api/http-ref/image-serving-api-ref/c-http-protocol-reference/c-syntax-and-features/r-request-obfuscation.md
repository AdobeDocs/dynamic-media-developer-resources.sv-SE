---
description: Innehållet i hela modifierardelen av begärandesträngen, inklusive det valfria låssuffixet, kan döljas genom att standardkodningen base64 används.
seo-description: Innehållet i hela modifierardelen av begärandesträngen, inklusive det valfria låssuffixet, kan döljas genom att standardkodningen base64 används.
seo-title: Förfrågan om obehörig
solution: Experience Manager
title: Förfrågan om obehörig
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Begär obehörig{#request-obfuscation}

Innehållet i hela modifierardelen av begärandesträngen, inklusive det valfria låssuffixet, kan döljas genom att standardkodningen base64 används.

Servern försöker avkoda om `attribute::RequestObfuscation` är inställt. Om avkodningen misslyckas avvisas begäran. Om både låsning av begäran och obstruktion av begäran används, måste låssuffixet genereras och läggas till före base64-kodning.

>[!IMPORTANT]
>
>Om du aktiverar den här funktionen bör du vara medveten om att det finns vissa begränsningar för dess användning som inkluderar följande:<br>- Dynamic Media användargränssnitt kanske inte visar rätt information för fältet **[!UICONTROL Last Published]**. Detta påverkar dock inte publiceringen.<br>- För närvarande fungerar inte HLS-videoströmning när **[!UICONTROL Request obfuscation]** och  **[!UICONTROL Request locking]** är aktiverat.<br>- För närvarande fungerar inte vissa Dynamic Media-visningsprogram när  **[!UICONTROL Request obfuscation]** och  **[!UICONTROL Request locking]** är aktiverade.

## Exempel {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

kodar till:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Alla förekomster av &#39;=&#39;, &#39;&amp;&#39; och &#39;%&#39; i värdesträngar måste föregås av kodningen &#39;%xx&#39; innan begäran döljs. Annars behöver du inte http-koda *modifierarna*-delen av begäran, antingen före eller efter dolda funktioner, även om låsning av begäran används, eftersom base64-kodning är säker för http-överföring.

## Se även {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP-kodning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7),  [Request Locking](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c),  [attribut::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
