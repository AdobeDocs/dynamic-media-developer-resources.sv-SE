---
description: Om text anges som svarsformat, formateras svarsdata så att de kan läsas som Java-egenskaper.
solution: Experience Manager
title: Textegenskaper (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
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
