---
description: Innehållet i hela modifierardelen av begärandesträngen, inklusive det valfria låssuffixet, kan döljas genom att standardkodningen base64 används.
solution: Experience Manager
title: Förfrågan om obehörig
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Förfrågan om obehörig{#request-obfuscation}

Innehållet i hela modifierardelen av begärandesträngen, inklusive det valfria låssuffixet, kan döljas genom att standardkodningen base64 används.

Servern försöker avkoda om `attribute::RequestObfuscation` har angetts. Om avkodningen misslyckas avvisas begäran. Om både låsning av begäran och obstruktion av begäran används, måste låssuffixet genereras och läggas till före base64-kodning.

>[!IMPORTANT]
>
>Om du aktiverar den här funktionen bör du vara medveten om att det finns vissa begränsningar för dess användning som omfattar följande:<br>- Dynamic Media användargränssnitt kanske inte visar rätt information för fältet **[!UICONTROL Last Published]**. Detta påverkar dock inte publiceringen.<br> - För närvarande fungerar inte HLS-videoströmning när **[!UICONTROL Request obfuscation]** och **[!UICONTROL Request locking]** är aktiverade.<br> - För närvarande fungerar inte vissa Dynamic Media-visningsprogram när **[!UICONTROL Request obfuscation]** och **[!UICONTROL Request locking]** är aktiverade.

## Exempel {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

kodar till:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Alla förekomster av &#39;=&#39;, &#39;&amp;&#39; och &#39;%&#39; i värdesträngar måste föregås av kodningen &#39;%xx&#39; innan begäran döljs. Annars behöver du inte http-koda *modifiers* -delen av begäran, antingen före eller efter förvrängning, även om begäran låses, eftersom base64-kodning är säker för http-överföring.

## Se även {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP-kodning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Begär låsning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribut::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
