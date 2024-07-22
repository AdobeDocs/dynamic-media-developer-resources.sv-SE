---
description: Om text anges som svarsformat, formateras svarsdata så att de kan läsas som Java-egenskaper.
solution: Experience Manager
title: Textegenskaper (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
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

Strängvärden kan innehålla escape-tecken i JAVA-format, till exempel `\n`, `\t`, `\:` eller `\\`.
