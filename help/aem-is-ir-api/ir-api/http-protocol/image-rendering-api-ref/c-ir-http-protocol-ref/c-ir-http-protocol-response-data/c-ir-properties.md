---
description: Egenskapsdata returneras som svar på följande req=-typer imageprops och props.
seo-description: Egenskapsdata returneras som svar på följande req=-typer imageprops och props.
seo-title: Egenskaper
solution: Experience Manager
title: Egenskaper
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# Egenskaper{#properties}

Egenskapsdata returneras som svar på följande req=-typer: bilproppar och proppar.

Svarsdata är formaterade så att de kan läsas som Java-egenskaper. Ett typiskt svar på textegenskaper har följande allmänna struktur:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` kan vara tom. Tomt utrymme är valfritt i början och slutet av varje rad och före och efter avgränsaren &#39;=&#39;. Enkla eller dubbla citattecken kan användas för att omsluta strängvärden, men är inte obligatoriska.

Strängvärden kan innehålla JAVA-liknande escape-tecken, som `\n`, `\t`, `\:`. eller `\\`.

**Se även**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
