---
description: Bildplatskoordinater som returneras av åtgärden getPhotoshopPath.
seo-description: Bildplatskoordinater som returneras av åtgärden getPhotoshopPath.
seo-title: PerspectiveQuad
solution: Experience Manager
title: PerspectiveQuad
uuid: e83b7b8c-995b-4ac0-ace5-491f7e98674d
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 9%

---


# PerspectiveQuad{#perspectivequad}

Bildplatskoordinater som returneras av åtgärden getPhotoshopPath.

Syntax

## Parametrar {#section-59792c446366456d90de7f5875bad1b0}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`x0`*` | `xsd:double` | Övre vänster x-axelkoordinat. |
| `*`y0`*` | `xsd:double` | Övre vänster y-axelkoordinat. |
| `*`x1`*` | `xsd:double` | Övre höger x-axelkoordinat. |
| `*`y1`*` | `xsd:double` | Övre höger y-axelkoordinat. |
| `*`x2`*` | `xsd:double` | Nedre höger x-axelkoordinat. |
| `*`y2`*` | `xsd:double` | Nedre höger y-axelkoordinat. |
| `*`x3`*` | `xsd:double` | Nedre vänster x-axelkoordinat. |
| `*`y3`*` | `xsd:double` | Nedre y-axelkoordinat. |

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

