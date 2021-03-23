---
description: Om text anges som svarsformat, formateras svarsdata så att de kan läsas som Java-egenskaper.
seo-description: Om text anges som svarsformat, formateras svarsdata så att de kan läsas som Java-egenskaper.
seo-title: Textegenskaper (Java)
solution: Experience Manager
title: Textegenskaper (Java)
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# Textegenskaper (Java){#text-java-properties}

Om text anges som svarsformat, formateras svarsdata så att de kan läsas som Java-egenskaper.

Ett typiskt svar på textegenskaper har följande allmänna struktur:

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* kan vara tom. Tomt utrymme är valfritt i början och slutet av varje rad och före och efter avgränsaren =. Enkla eller dubbla citattecken kan användas för att omsluta strängvärden, men är inte obligatoriska.

Strängvärden kan innehålla escape-tecken i JAVA-format, t.ex. `\n`, `\t`, `\:` eller `\\`.
