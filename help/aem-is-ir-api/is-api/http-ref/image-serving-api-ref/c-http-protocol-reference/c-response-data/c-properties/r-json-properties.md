---
title: JSONP-egenskaper
description: Om jsonp anges som svarsformat formateras svarsdata med JSONP (JavaScript Object Notation with Padding), som omsluts av ett JavaScript-funktionsanrop.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# JSONP-egenskaper{#jsonp-properties}

Om jsonp anges som svarsformat formateras svarsdata med JSONP (JavaScript Object Notation with Padding), som omsluts av ett JavaScript-funktionsanrop.

Klienten kan ange en valfri unik begärandeidentifierare ( *`reqId`*) som returneras i svaret och gör att klienten kan särskilja flera svar som tas emot asynkront. Ett typiskt svar har följande allmänna struktur:

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

JavaScript-funktionen `s7jsonResponse` måste definieras av klienten. I den enklaste formen kan funktionen se ut så här:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Begäranden som har stöd för JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler]`

Syntaxen `<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.

Paketet Dynamic Media Image Serving Viewers innehåller ett verktyg för att begära och analysera JSONP-formaterade data från Image Serving.

Mer information om JSONP-formatet finns i [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP).

Mer information om JSON-formatet finns i [www.json.org](https://www.json.org/json-en.html).

Se även [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
