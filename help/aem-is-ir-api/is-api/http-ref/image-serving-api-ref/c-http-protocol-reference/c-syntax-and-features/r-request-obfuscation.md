---
description: Innehållet i hela modifierardelen av begärandesträngen, inklusive det valfria låssuffixet, kan döljas genom att standardkodningen base64 används.
seo-description: Innehållet i hela modifierardelen av begärandesträngen, inklusive det valfria låssuffixet, kan döljas genom att standardkodningen base64 används.
seo-title: Förfrågan om obehörig
solution: Experience Manager
title: Förfrågan om obehörig
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 80ae3a549340156bb74faa1793c43d3a8fa3853c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Förfrågan om obehörig{#request-obfuscation}

Innehållet i hela modifierardelen av begärandesträngen, inklusive det valfria låssuffixet, kan döljas genom att standardkodningen base64 används.

Servern försöker avkoda om `attribute::RequestObfuscation` den är inställd. Om avkodningen misslyckas avvisas begäran. Om både låsning av begäran och obstruktion av begäran används, måste låssuffixet genereras och läggas till före base64-kodning.

>[!IMPORTANT]
>
>Om du aktiverar den här funktionen bör du vara medveten om att det finns vissa begränsningar för dess användning som omfattar följande:<br>- Användargränssnittet för dynamiska media kanske inte visar rätt information för **[!UICONTROL Last Published]** fältet. Detta påverkar dock inte publiceringen.<br>- För närvarande fungerar inte HLS-videoströmning när **[!UICONTROL Request obfuscation]** och **[!UICONTROL Request locking]** är aktiverat.

## Exempel {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

kodar till:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Alla förekomster av &#39;=&#39;, &#39;&amp;&#39; och &#39;%&#39; i värdesträngar måste föregås av kodningen &#39;%xx&#39; innan begäran döljs. Annars behöver du inte http-koda *modifierarna* i begäran, antingen före eller efter förvrängning, även om begäranlåsning används, eftersom base64-kodning är säker för http-överföring.

## Se även {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP-kodning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Request Locking](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribut::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
