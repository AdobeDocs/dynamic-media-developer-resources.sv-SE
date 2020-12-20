---
description: För att minska risken för manipulering av förfrågningar finns det en enkel låsfunktion.
seo-description: För att minska risken för manipulering av förfrågningar finns det en enkel låsfunktion.
seo-title: Begäranlåsning
solution: Experience Manager
title: Begäranlåsning
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---


# Begäranlåsning{#request-locking}

För att minska risken för manipulering av förfrågningar finns det en enkel låsfunktion.

Om attribute::RequestLock är inställt måste ett låsvärde läggas till i begäran, i formatet `&xxxx`, där xxxx är ett fyrsiffrigt hexvärde. Det här hexvärdet genereras med en enkel hash-algoritm som används för *modifierarna*-delen av begäran (efter &#39;?&#39; som skiljer URL-sökvägen från *modifierare*). Detta måste göras efter att begäran är fullständigt http-kodad, men innan den (valfritt) är okomplicerad. När begäran har avfaltats kommer servern att använda samma algoritm för modifieringssträngen (förutom de sista 5 tecknen, som innehåller låsvärdet). Om den genererade nyckeln inte matchar låset avvisas begäran.

>[!IMPORTANT]
>
>Om du aktiverar den här funktionen bör du vara medveten om att det finns vissa begränsningar för dess användning som inkluderar följande:<br>- Dynamic Media användargränssnitt kanske inte visar rätt information för fältet **[!UICONTROL Last Published]**. Detta påverkar dock inte publiceringen.<br>- För närvarande fungerar inte HLS-videoströmning när **[!UICONTROL Request obfuscation]** och  **[!UICONTROL Request locking]** är aktiverat.<br>- För närvarande fungerar inte vissa Dynamic Media-visningsprogram när  **[!UICONTROL Request obfuscation]** och  **[!UICONTROL Request locking]** är aktiverade.

C++-exempelkod för att generera begäranlåsningsvärdet:

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## Se även {#section-a6d45406c0354669ac581793e4fa8436}

[HTTP-kodning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7),  [Request Obfuscation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d),  [attribut::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
