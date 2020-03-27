---
description: Tar bort ett bildformat. Hämta bildformatshandtaget från saveImageFormat.
seo-description: Tar bort ett bildformat. Hämta bildformatshandtaget från saveImageFormat.
seo-title: deleteImageFormat
solution: Experience Manager
title: deleteImageFormat
topic: Scene7 Image Production System API
uuid: 70dddde9-830b-4267-8ef5-df5241f549e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteImageFormat{#deleteimageformat}

Tar bort ett bildformat. Hämta bildformatshandtaget från saveImageFormat.

Syntax

## Auktoriserade användartyper {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-462c05d9aad746ee8d2be0656041b693}

**Indata (deleteImageFormatParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget som innehåller det bildformat som du vill ta bort. |
| ` *`imageFormatHandle`*` | `xsd:string` | Ja | Handtaget till det bildformat som du vill ta bort. |

**Utdata (deleteImageFormatParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Det här kodexemplet tar bort ett bildformat från ett företag. Hämta bildformatshandtaget från en annan åtgärd.

**Begäran**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**Svar**

Ingen.

**Relaterat ämne:**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
