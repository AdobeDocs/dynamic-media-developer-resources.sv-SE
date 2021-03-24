---
description: Egenskapsdata returneras som svar på följande req=-typer imageprops och props.
solution: Experience Manager
title: Egenskaper
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
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
