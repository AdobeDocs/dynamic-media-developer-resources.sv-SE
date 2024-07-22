---
title: JavaScript-egenskaper
description: Om JavaScript anges som svarsformat formateras svarsdata så att de tolkas som en JavaScript&trade; include-fil.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# JavaScript-egenskaper{#javascript-properties}

Om JavaScript anges som svarsformat formateras svarsdata så att de tolkas som en JavaScript include-fil.

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

*`propertyValue`* kan vara tom. Tomt utrymme är valfritt i början och slutet av varje rad och före och efter avgränsaren =. Alla värden omges av enkla citattecken. Enkla citattecken i strängar föregås av två på varandra följande enkla citattecken.

Om du vill tolka ett JavaScript-egenskapssvar måste alla objekt som svaret refererar till skapas innan egenskapsfilen läses in. Här följer ett exempel på hur du använder `req=props` för att få fram svarsbildens storlek i JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
