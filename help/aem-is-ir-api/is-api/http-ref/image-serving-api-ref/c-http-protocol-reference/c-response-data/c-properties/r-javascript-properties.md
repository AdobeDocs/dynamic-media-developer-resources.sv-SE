---
description: Om JavaScript™ anges som svarsformat formateras svarsdata så att de tolkas som en JavaScript™-inkluderingsfil.
solution: Experience Manager
title: JavaScript™-egenskaper
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# JavaScript™-egenskaper{#javascript-properties}

Om JavaScript™ anges som svarsformat formateras svarsdata så att de tolkas som en JavaScript™-inkluderingsfil.

Ett typiskt JavaScript™-egenskapssvar har följande allmänna struktur:

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

Om du vill analysera ett JavaScript™-egenskapssvar måste alla objekt eller objekt som svaret refererar till skapas innan egenskapsfilen läses in. Här följer ett exempel på hur du använder `req=props` för att få svarsbildens storlek i JavaScript™:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

