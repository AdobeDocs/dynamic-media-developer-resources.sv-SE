---
description: Om jsonp anges som svarsformat formateras svarsdata med JSONP (JavaScript Object Notation with Padding), som omsluts av ett JavaScript-funktionsanrop.
seo-description: Om jsonp anges som svarsformat formateras svarsdata med JSONP (JavaScript Object Notation with Padding), som omsluts av ett JavaScript-funktionsanrop.
seo-title: JSONP-egenskaper
solution: Experience Manager
title: JSONP-egenskaper
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '239'
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

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.

Paketet Dynamic Media Image Serving Viewers innehåller ett verktyg för att begära och analysera JSONP-formaterade data från Image Serving.

Mer information om JSONP-formatet finns i [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP).

Mer information om JSON-formatet finns i [www.json.org](http://www.json.org).

Se även [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
