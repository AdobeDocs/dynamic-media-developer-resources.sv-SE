---
description: Om xml anges som svarsformat formateras svarsdata som ett XML-dokument som kan tolkas av alla vanliga XML-tolkar.
seo-description: Om xml anges som svarsformat formateras svarsdata som ett XML-dokument som kan tolkas av alla vanliga XML-tolkar.
seo-title: XML-egenskaper
solution: Experience Manager
title: XML-egenskaper
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# XML-egenskaper{#xml-properties}

Om xml anges som svarsformat formateras svarsdata som ett XML-dokument som kan tolkas av alla vanliga XML-tolkar.

Ett typiskt egenskapssvarsdokument har följande allmänna struktur:

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

`<prop-group>`-elementet används som den yttersta behållaren och för grupperingsegenskaper. Om en grupp har namnet motsvarar namnet Java-/JavaScript-objektnamnet.

>[!NOTE]
>
>Teckenkodning kan anges för vissa `req=`-typer. Mer information finns i beskrivningen av det specifika `req=`kommandot.

