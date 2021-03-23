---
description: Om xml anges som svarsformat formateras svarsdata som ett XML-dokument som kan tolkas av alla vanliga XML-tolkar.
seo-description: Om xml anges som svarsformat formateras svarsdata som ett XML-dokument som kan tolkas av alla vanliga XML-tolkar.
seo-title: XML-egenskaper
solution: Experience Manager
title: XML-egenskaper
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
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

