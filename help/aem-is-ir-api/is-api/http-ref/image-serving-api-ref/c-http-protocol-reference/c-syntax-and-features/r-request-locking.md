---
description: För att minska risken för manipulering av förfrågningar finns det en enkel låsfunktion.
solution: Experience Manager
title: Begäranlåsning
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Begäranlåsning{#request-locking}

För att minska risken för manipulering av förfrågningar finns det en enkel låsfunktion.

Om attribute::RequestLock är inställt måste ett låsvärde läggas till i begäran i form av `&xxxx`, där xxxx är ett fyrsiffrigt hexvärde. Det här hexadecimala värdet genereras med en enkel hash-algoritm som tillämpas på *modifierare* del av begäran (efter &#39;?&#39; som skiljer URL-sökvägen från *modifierare*). Detta måste göras efter att begäran är fullständigt http-kodad, men innan den (valfritt) är okomplicerad. När begäran har avfaltats kommer servern att använda samma algoritm för modifieringssträngen (förutom de sista 5 tecknen, som innehåller låsvärdet). Om den genererade nyckeln inte matchar låset avvisas begäran.

>[!IMPORTANT]
>
>Om du aktiverar den här funktionen bör du vara medveten om att det finns vissa begränsningar för dess användning som omfattar följande:<br>- Dynamic Media användargränssnitt kanske inte visar rätt information för **[!UICONTROL Last Published]** fält. Detta påverkar dock inte publiceringen.<br>- För närvarande fungerar inte HLS-videoströmning när **[!UICONTROL Request obfuscation]** och **[!UICONTROL Request locking]** är aktiverade.<br>- För närvarande fungerar inte vissa Dynamic Media-visningsprogram när **[!UICONTROL Request obfuscation]** och **[!UICONTROL Request locking]** är aktiverade.

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

[HTTP-kodning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Förfrågningsfel](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
