---
description: Om xml anges som svarsformat formateras svarsdata som ett XML-dokument som kan tolkas av alla vanliga XML-tolkar.
solution: Experience Manager
title: XML-egenskaper
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
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

The `<prop-group>` -elementet används som den yttersta behållaren och för grupperingsegenskaper. Om en grupp har namnet motsvarar namnet Java-/JavaScript-objektnamnet.

>[!NOTE]
>
>Teckenkodning kan anges för vissa `req=` typer. Se beskrivningen av den specifika `req=`om du vill ha mer information.
