---
description: För att minska risken för manipulering av förfrågningar finns det en enkel låsfunktion.
seo-description: För att minska risken för manipulering av förfrågningar finns det en enkel låsfunktion.
seo-title: Begäranlåsning
solution: Experience Manager
title: Begäranlåsning
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Begäranlåsning{#request-locking}

För att minska risken för manipulering av förfrågningar finns det en enkel låsfunktion.

Om attribute::RequestLock anges måste ett låsvärde läggas till i begäran, i form av `&xxxx`, där xxxx är ett fyrsiffrigt hexvärde. Det här hex-värdet genereras med en enkel hash-algoritm som tillämpas på *modifierardelen* i begäran (efter &#39;?&#39; som skiljer URL-sökvägen från *modifierarna*). Detta måste göras efter att begäran är fullständigt http-kodad, men innan den (valfritt) är okomplicerad. När begäran har avfaltats kommer servern att använda samma algoritm för modifieringssträngen (förutom de sista 5 tecknen, som innehåller låsvärdet). Om den genererade nyckeln inte matchar låset avvisas begäran.

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

[HTTP-kodning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Request Obfuscation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribut::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
