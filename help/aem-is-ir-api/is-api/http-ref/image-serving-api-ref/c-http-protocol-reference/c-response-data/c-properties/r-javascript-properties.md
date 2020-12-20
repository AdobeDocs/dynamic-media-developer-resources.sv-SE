---
description: Om javascript anges som svarsformat formateras svarsdata så att de tolkas som en inkluderingsfil för JavaScript.
seo-description: Om javascript anges som svarsformat formateras svarsdata så att de tolkas som en inkluderingsfil för JavaScript.
seo-title: JavaScript-egenskaper
solution: Experience Manager
title: JavaScript-egenskaper
topic: Scene7 Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# JavaScript-egenskaper{#javascript-properties}

Om javascript anges som svarsformat formateras svarsdata så att de tolkas som en inkluderingsfil för JavaScript.

Ett typiskt JavaScript-egenskapssvar har följande allmänna struktur:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* kan vara tom. Tomt utrymme är valfritt i början och slutet av varje rad och före och efter avgränsaren =. Alla värden omges av enkla citattecken. Enkla citattecken i strängar escape-konverteras med två på varandra följande enkla citattecken.

Om du vill analysera ett JavaScript-egenskapssvar måste alla objekt som svaret refererar till skapas innan egenskapsfilen läses in. Här följer ett exempel på hur du använder `req=props` för att få svarsbildens storlek i JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

