---
description: Om xml anges som svarsformat formateras svarsdata som ett XML-dokument som kan tolkas av alla vanliga XML-tolkar.
solution: Experience Manager
title: XML-egenskaper
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '117'
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

