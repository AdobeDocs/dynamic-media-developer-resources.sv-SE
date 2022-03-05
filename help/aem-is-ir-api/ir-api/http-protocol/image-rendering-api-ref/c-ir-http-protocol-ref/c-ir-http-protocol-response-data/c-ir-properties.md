---
title: Egenskaper
description: Egenskapsdata returneras som svar på följande req=-typer imageprops och props.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Egenskaper{#properties}

Egenskapsdata returneras som svar på följande req=-typer: bilproppar och proppar.

Svarsdata är formaterade så att de kan läsas som Java™-egenskaper. Ett typiskt svar på textegenskaper har följande allmänna struktur:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` Kan vara tomt. Tomt utrymme är valfritt i början och slutet av varje rad och före och efter avgränsaren &#39;=&#39;. Enkla eller dubbla citattecken kan användas för att omsluta strängvärden, men är inte obligatoriska.

Strängvärden kan innehålla escape-tecken i JAVA-format, t.ex. `\n`, `\t`, `\:`, eller `\\`.

**Se även**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
