---
description: Bildplatskoordinater som returneras av åtgärden getPhotoshopPath.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

Bildplatskoordinater som returneras av åtgärden getPhotoshopPath.

Syntax

## Parametrar {#section-59792c446366456d90de7f5875bad1b0}

| Namn | Typ | Beskrivning |
|---|---|---|
| x0 | `xsd:double` | Övre vänster x-axelkoordinat. |
| y0 | `xsd:double` | Övre vänster y-axelkoordinat. |
| x1 | `xsd:double` | Övre höger x-axelkoordinat. |
| y1 | `xsd:double` | Övre höger y-axelkoordinat. |
| x2 | `xsd:double` | Nedre höger x-axelkoordinat. |
| y2 | `xsd:double` | Nedre höger y-axelkoordinat. |
| x3 | `xsd:double` | Nedre vänster x-axelkoordinat. |
| y3 | `xsd:double` | Nedre y-axelkoordinat. |

## Exempel {#section-19ed4409ff3a41c9b52a9c9424612927}

Typen `PerspectiveQuad` returnerar data i den här ordningen:

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)
