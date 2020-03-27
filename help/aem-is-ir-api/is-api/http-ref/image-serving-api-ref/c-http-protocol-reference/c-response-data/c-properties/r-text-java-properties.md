---
description: Om text anges som svarsformat, formateras svarsdata så att de kan läsas som Java-egenskaper.
seo-description: Om text anges som svarsformat, formateras svarsdata så att de kan läsas som Java-egenskaper.
seo-title: Textegenskaper (Java)
solution: Experience Manager
title: Textegenskaper (Java)
topic: Scene7 Image Serving - Image Rendering API
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

Strängvärden kan innehålla escape-tecken av JAVA-typ, till exempel `\n`, `\t`, `\:`eller `\\`.
